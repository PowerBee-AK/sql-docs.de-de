---
description: '&#x40;&#x40;FETCH_STATUS (Transact-SQL)'
title: FETCH_STATUS (Transact-SQL)
ms.custom: ''
ms.date: 09/18/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- '@@FETCH_STATUS'
- '@@FETCH_STATUS_TSQL'
dev_langs:
- TSQL
helpviewer_keywords:
- FETCH statement
- status information [SQL Server], FETCH
- '@@FETCH_STATUS function'
ms.assetid: 93659193-e4ff-4dfb-9043-0c4114921b91
author: cawrites
ms.author: chadam
ms.openlocfilehash: 2a3bed4ab14d6efc43ae208523118bb063c39967
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187791"
---
# <a name="x40x40fetch_status-transact-sql"></a>&#x40;&#x40;FETCH_STATUS (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

Diese Funktion gibt den Status der letzten Cursor-FETCH-Anweisung zurück, die für einen beliebigen der aktuell von der Verbindung geöffneten Cursor ausgegeben wurde.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
@@FETCH_STATUS  
```  

[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="return-type"></a>Rückgabetyp  
 **integer**  
  
## <a name="return-value"></a>Rückgabewert  
  
|Rückgabewert|BESCHREIBUNG|  
|------------------|-----------------|  
|&nbsp;0|Die FETCH-Anweisung war erfolgreich.|  
|-1|Die FETCH-Anweisung ist fehlgeschlagen, oder die Zeile war außerhalb des Resultsets.|  
|-2|Die abgerufene Zeile fehlt.|
|–9|Der Cursor führt keinen Abrufvorgang aus.|  
  
## <a name="remarks"></a>Hinweise  
Da `@@FETCH_STATUS` global für alle Cursor bei einer Verbindung gilt, verwenden Sie dies mit Bedacht. Nachdem eine FETCH-Anweisung ausgeführt wurde, muss der Test für `@@FETCH_STATUS` durchgeführt werden, bevor eine weitere FETCH-Anweisung für einen anderen Cursor ausgeführt wird. `@@FETCH_STATUS` wird erst definiert, wenn ein Abrufvorgang für die Verbindung ausgeführt wurde.  
  
Ein Benutzer führt z.B. eine FETCH-Anweisung von einem Cursor aus durch und ruft dann eine gespeicherte Prozedur auf, die die Ergebnisse von einem anderen Cursor aus öffnet und verarbeitet. Wenn die Steuerung von der aufgerufenen gespeicherten Prozedur zurückgegeben wird, spiegelt `@@FETCH_STATUS` die letzte in der Prozedur ausgeführte FETCH-Anweisung wider und nicht die FETCH-Anweisung, die vor dem Aufruf der gespeicherten Prozedur ausgeführt wurde.  
  
Um den letzten FETCH-Status eines bestimmten Cursors abzurufen, führen Sie eine Abfrage der **fetch_status**-Spalte in der dynamischen Verwaltungsfunktion **sys.dm_exec_cursors** durch.  
  
## <a name="examples"></a>Beispiele  
In diesem Beispiel wird `@@FETCH_STATUS` zur Steuerung der Cursoraktivitäten in einer `WHILE`-Schleife verwendet.  
  
```sql  
DECLARE Employee_Cursor CURSOR FOR  
SELECT BusinessEntityID, JobTitle  
FROM AdventureWorks2012.HumanResources.Employee;  
OPEN Employee_Cursor;  
FETCH NEXT FROM Employee_Cursor;  
WHILE @@FETCH_STATUS = 0  
   BEGIN  
      FETCH NEXT FROM Employee_Cursor;  
   END;  
CLOSE Employee_Cursor;  
DEALLOCATE Employee_Cursor;  
GO  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Cursorfunktionen &#40;Transact-SQL&#41;](../../t-sql/functions/cursor-functions-transact-sql.md)   
 [FETCH &#40;Transact-SQL&#41;](../../t-sql/language-elements/fetch-transact-sql.md)  
  
  
