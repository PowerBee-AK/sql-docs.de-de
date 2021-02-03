---
description: MSSQLSERVER_5237
title: MSSQLSERVER_5237 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 5237 (Database Engine error)
ms.assetid: 9ff28935-d1eb-47ee-99b3-1a65cb948ce7
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 78b86d7c3e8d30db48496fcf33c1d970c751b391
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99198119"
---
# <a name="mssqlserver_5237"></a>MSSQLSERVER_5237
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|5237|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|DBCC4_INDEXED_VIEW_CHECK_QUERY_FAILED_NO_ERRORCODE|  
|Meldungstext|Fehler bei der rowsetübergreifenden DBCC-Überprüfung für das 'NAME'-Objekt (Objekt-ID O_ID) aufgrund eines internen Abfragefehlers.|  
  
## <a name="explanation"></a>Erklärung  
Ein interner Fehler ist aufgetreten, weil DBCC die Abfrage zum Überprüfen indizierter Sichten nicht ausführen konnte.  
  
## <a name="user-action"></a>Benutzeraktion  
Führen Sie den DBCC-Befehl erneut aus.  
  
