---
description: MSSQLSERVER_10003
title: MSSQLSERVER_10003 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 10003 (Database Engine error)
ms.assetid: 9e2cb199-f077-4d88-8117-1b7550afc696
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 81fb97c6cb16bacddfdbfacf63821e8aaac050b4
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197523"
---
# <a name="mssqlserver_10003"></a>MSSQLSERVER_10003
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|10003|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|HR_E_OUTOFMEMORY|  
|Meldungstext|Dem Anbieter steht nicht genügend Arbeitsspeicher zur Verfügung.|  
  
## <a name="explanation"></a>Erklärung  
Zu geringer Systemspeicher hat bewirkt, dass der OLE DB-Anbieter nicht mehr über genügend Speicher verfügt.  
  
## <a name="user-action"></a>Benutzeraktion  
Starten Sie die Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]neu. Falls der Fehler dadurch nicht behoben wird, starten Sie den Computer neu. Wenn das Problem weiterhin auftritt, listen Sie OLE DB-Ablaufverfolgungsereignisse mit [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] auf, und stellen Sie diese Daten für den Produktsupport des OLE DB-Anbieters bereit.  
  
## <a name="see-also"></a>Weitere Informationen  
[Vorlagen und Berechtigungen in SQL Server Profiler](~/tools/sql-server-profiler/sql-server-profiler-templates-and-permissions.md)  
[SQL Server Native Client &#40;OLE DB&#41;](~/relational-databases/native-client/ole-db/sql-server-native-client-ole-db.md)  
  
