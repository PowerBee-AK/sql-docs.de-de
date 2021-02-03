---
description: MSSQLSERVER_17884
title: MSSQLSERVER_17884 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 17884 (Database Engine error)
ms.assetid: 8d05ba05-3f71-4dc3-bd81-2ea5ac9fe843
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 5e81871694060414d0f3fdf24fde05b01d0b13d8
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99196593"
---
# <a name="mssqlserver_17884"></a>MSSQLSERVER_17884
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|17884|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|SRV_SCHEDULER_DEADLOCK|  
|Meldungstext|Neue Abfragen, die dem Prozess im %d-Knoten zugewiesen sind, wurden in den letzten %d Sekunden von keinem Arbeitsthread abgerufen. Die Ursache hierfür können blockierende Abfragen oder Abfragen mit langer Ausführungszeit sein, wodurch die Clientantwortzeit beeinträchtigt wird. Erhöhen Sie mithilfe der Konfigurationsoption „Max. Anzahl von Arbeitsthreads“ die Anzahl zulässiger Threads, oder optimieren Sie aktuell ausgeführte Abfragen.  SQL-Prozessnutzung: %d%%. Leerlauf des Systems: %d%%.|  
  
## <a name="explanation"></a>Erklärung  
In den Zeitplanungsmodulen gibt es kein Anzeichen von Fortschritt. Die Ursache können Deadlocks sein, bei denen keine Threads fortgeführt werden können und/oder keine neue Arbeit aufgenommen und verarbeitet werden kann. Wenn die Prozessnutzung niedrig ist, können andere Prozesse auf dem Computer möglicherweise dazu führen, dass auf die Serverprozess-CPU nicht mehr zugegriffen werden kann.  
  
## <a name="user-action"></a>Benutzeraktion  
Bestimmen Sie die Ursache für die Blockierung und den fehlenden Fortschritt, und lösen Sie die Situation entsprechend. Wenn die Prozessnutzung niedrig ist, prüfen Sie die Systemlast, die von anderen Prozessen verursacht wird.  
  
