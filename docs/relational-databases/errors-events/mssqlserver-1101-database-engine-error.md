---
description: MSSQLSERVER_1101
title: MSSQLSERVER_1101 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 1101 (Database Engine error)
ms.assetid: d63b67d5-59f5-4f77-904e-5ba67f2dd850
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 4927e306ff355413dd81c72420a760102ea1043f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197219"
---
# <a name="mssqlserver_1101"></a>MSSQLSERVER_1101
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|1101|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|NOALLOCPG|  
|Meldungstext|Eine neue Seite für die '%.*ls'-Datenbank konnte nicht zugeordnet werden, weil in der Dateigruppe '%.\*ls' nicht genügend Speicherplatz verfügbar ist. Speicherplatz kann durch Löschen von Objekten in der Dateigruppe, Hinzufügen von Dateien zur Dateigruppe oder Festlegen der automatischen Vergrößerung für vorhandene Dateien in der Dateigruppe gewonnen werden.|  
  
## <a name="explanation"></a>Erklärung  
In einer Dateigruppe ist kein Speicherplatz verfügbar.  
  
## <a name="user-action"></a>Benutzeraktion  
Durch die folgenden Aktionen kann Speicherplatz in der Dateigruppe verfügbar gemacht werden.  
  
-   Aktivieren Sie AUTOGROW.  
  
-   Fügen Sie der Dateigruppe weitere Dateien hinzu.  
  
-   Geben Sie Speicherplatz frei, indem sich nicht benötigte Indizes oder Tabellen in der Dateigruppe löschen.  
  
