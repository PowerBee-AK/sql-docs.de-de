---
description: MSSQLSERVER_17067
title: MSSQLSERVER_17067 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 17067 (Database Engine error)
ms.assetid: 32c1f0e8-db70-4836-95b2-8833be9e0ad1
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 785e389dee61a90650d325becd678f998a75da9b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99196828"
---
# <a name="mssqlserver_17067"></a>MSSQLSERVER_17067
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|17067|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|SQLASSERT_MESG|  
|Meldungstext|SQL Server-Assertion: Datei: \<%s>, Zeile = %d %s. Dieser Fehler hängt möglicherweise mit dem Ausführungszeitpunkt zusammen. Wenn der Fehler nach dem erneuten Ausführen der Anweisung weiterhin auftritt, überprüfen Sie die Datenbank mit DBCC CHECKDB auf strukturelle Integrität, oder starten Sie den Server neu, um sicherzustellen, dass keine speicherresidenten Datenstrukturen beschädigt sind.|  
  
## <a name="explanation"></a>Erklärung  
Dieser Fehler kann von vorübergehenden Zeitsteuerungsfehlern oder durch Datenbeschädigung im Speicher oder auf dem Datenträger verursacht werden.  
  
## <a name="user-action"></a>Benutzeraktion  
Führen Sie die Anweisung, die die Ausnahme ausgelöst hat, erneut aus. Wenn der Fehler von einem Zeitsteuerungsereignis verursacht wurde, tritt er möglicherweise nicht wieder auf. Wenn das Problem weiterhin auftritt, führen Sie DBCC CHECKDB zur Überprüfung auf Beschädigungen auf dem Datenträger aus. Starten Sie den Server neu, um sicherzustellen, dass die speicherinternen Datenstrukturen nicht beschädigt sind.  
  
## <a name="see-also"></a>Weitere Informationen  
[DBCC CHECKDB &#40;Transact-SQL&#41;](~/t-sql/database-console-commands/dbcc-checkdb-transact-sql.md)  
  
