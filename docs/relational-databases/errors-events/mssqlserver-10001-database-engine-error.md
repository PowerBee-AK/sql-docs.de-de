---
description: MSSQLSERVER_10001
title: MSSQLSERVER_10001 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 10001 (Database Engine error)
ms.assetid: f8fd2d8d-a4af-4b6a-ba51-9123b7e4c9bf
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 92f3b862798dd54f782834c86d724a1a591c1d4f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197544"
---
# <a name="mssqlserver_10001"></a>MSSQLSERVER_10001
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|10001|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|HR_E_UNEXPECTED|  
|Meldungstext|Der Anbieter hat einen unerwarteten schwerwiegenden Fehler gemeldet.|  
  
## <a name="explanation"></a>Erklärung  
Bei der Verarbeitung von verteilten Abfragen ist ein generischer Fehler beim Aufrufen des OLE DB-Anbieters aufgetreten.  
  
## <a name="user-action"></a>Benutzeraktion  
Listen Sie OLE DB-Ablaufverfolgungsereignisse mit [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] auf, und stellen Sie diese Daten für den Produktsupport des OLE DB-Anbieters bereit.  
  
## <a name="see-also"></a>Weitere Informationen  
[Vorlagen und Berechtigungen in SQL Server Profiler](~/tools/sql-server-profiler/sql-server-profiler-templates-and-permissions.md)  
[SQL Server Native Client &#40;OLE DB&#41;](~/relational-databases/native-client/ole-db/sql-server-native-client-ole-db.md)  
  
