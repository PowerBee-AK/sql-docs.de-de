---
description: APP_NAME (Transact-SQL)
title: APP_NAME (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 07/24/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- APP_NAME_TSQL
- APP_NAME
dev_langs:
- TSQL
helpviewer_keywords:
- name checking for current session [SQL Server]
- sessions [SQL Server], application names
- applications [SQL Server], names
- current session application names
- APP_NAME function
ms.assetid: e491e192-9b30-4243-bc19-33c133fe08a8
author: cawrites
ms.author: chadam
ms.openlocfilehash: d41dd7e7e7c435b627be4c9b60a32a9869eadae1
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99211493"
---
# <a name="app_name-transact-sql"></a>APP_NAME (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

Diese Funktion gibt den Anwendungsnamen der aktuellen Sitzung zurück, falls die Anwendung diesen Namenswert festlegt.
  
> [!IMPORTANT]  
>  Der Client stellt den Anwendungsnamen zur Verfügung. `APP_NAME` überprüft den Anwendungsnamenswert nicht. Verwenden Sie `APP_NAME` nicht als Teil einer Sicherheitsprüfung.  
  
![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
APP_NAME  ( )  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="return-types"></a>Rückgabetypen
**nvarchar(128)**
  
## <a name="remarks"></a>Hinweise  
Verwenden Sie `APP_NAME`, um zwischen den verschiedenen Anwendungen zu unterscheiden, damit Sie verschiedene Aktionen für diese Anwendung durchführen können. `APP_NAME` kann beispielsweise zwischen verschiedenen Anwendungen unterscheiden, damit für jede Anwendung ein anderes Datumsformat verwendet werden kann. Außerdem kann durch diese Funktion eine Nachricht mit Informationen an bestimmte Anwendungen zurückgegeben werden.
  
Klicken Sie zum Festlegen eines Anwendungsnamens in [!INCLUDE[ssManStudio](../../includes/ssmanstudio-md.md)] im Dialogfeld **Verbindung mit Datenbank-Engine** herstellen auf **Optionen**. Geben Sie auf der Registerkarte **Zusätzliche Verbindungsparameter** das Attribut **app** im Format `;app='application_name'` an.
  
## <a name="example"></a>Beispiel  
Im folgenden Beispiel wird geprüft, ob die Clientanwendung, die diesen Prozess initiiert hat, eine `SQL Server Management Studio`-Sitzung ist. Dann wird ein Datumswert im US- oder ANSI-Format bereitgestellt.
  
```sql
USE AdventureWorks2012;  
GO  
IF APP_NAME() = 'Microsoft SQL Server Management Studio - Query'  
PRINT 'This process was started by ' + APP_NAME() + '. The date is ' + CONVERT ( VARCHAR(100) , GETDATE(), 101) + '.';  
ELSE   
PRINT 'This process was started by ' + APP_NAME() + '. The date is ' + CONVERT ( VARCHAR(100) , GETDATE(), 102) + '.';  
GO  
```  
  
## <a name="see-also"></a>Siehe auch
[Systemfunktionen &#40;Transact-SQL&#41;](../../relational-databases/system-functions/system-functions-category-transact-sql.md)  
[Funktionen](../../t-sql/functions/functions.md)
  
  
