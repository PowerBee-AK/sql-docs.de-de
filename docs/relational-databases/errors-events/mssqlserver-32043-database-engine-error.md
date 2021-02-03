---
description: MSSQLSERVER_32043
title: MSSQLSERVER_32043 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 32043 (Database Engine error)
ms.assetid: a0c48ae3-4c8c-419c-afb5-579fcefac01d
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 14e12c039a6e7a8fdee8504f84008db05c710c75
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99200206"
---
# <a name="mssqlserver_32043"></a>MSSQLSERVER_32043
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|32043|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|SQLErrorNum32043|  
|Meldungstext|Die Warnung für 'nicht wiederhergestelltes Protokoll' wurde ausgelöst. Der aktuelle Wert von '%d' überschreitet den Threshold '%d'.|  
  
## <a name="explanation"></a>Erklärung  
Dieses Ereignis der Datenbankspiegelung wird für die Spiegelserverinstanz ausgelöst, um anzugeben, dass der Umfang des nicht wiederhergestellten Protokolls einen vom Benutzer angegebenen Schwellenwert erreicht hat. Normalerweise tritt dieses Ereignis auf, weil sich die Leistung des Systems geändert hat. Entweder hat sich die Bandbreite zwischen den beiden Systemen reduziert, oder die Last hat sich erhöht.  
  
Ein nicht wiederhergestelltes Protokoll ist ein Protokoll, das von der Spiegelserverinstanz empfangen und auf einen Datenträger geschrieben wurde, das jedoch noch für die Spiegeldatenbank wiederhergestellt werden muss. Der Umfang des nicht wiederhergestellten Protokolls in Kilobyte (KB) ist eine Leistungsmetrik, mit der Sie die aktuelle Failoverzeit abschätzen können. Die zum Übernehmen des nicht wiederhergestellten Protokolls erforderliche Zeit stellt den Hauptfaktor der Failoverzeit dar – zusammen mit einer kurzen zusätzlichen Zeit, die erforderlich ist, um die Datenbank wiederherzustellen und sie online zu schalten.  
  
> [!NOTE]  
> Bei einem automatischen Failover ist die Zeit, die das System benötigt, um den Fehler zu erkennen, unabhängig von der Failoverzeit.  
  
## <a name="user-action"></a>Benutzeraktion  
Prüfen Sie die Auslastung für die Instanzen des Prinzipalservers und des Spiegelservers sowie die entsprechenden Netzwerkverbindungen, um die Ursache zu ermitteln.  
  
## <a name="see-also"></a>Weitere Informationen  
[Datenbankspiegelung &#40;SQL Server&#41;](~/database-engine/database-mirroring/database-mirroring-sql-server.md)  
[Verwenden von Warnungsschwellenwerten und Warnmeldungen für Spiegelungsleistungsmetriken &#40;SQL Server&#41;](~/database-engine/database-mirroring/use-warning-thresholds-and-alerts-on-mirroring-performance-metrics-sql-server.md)  
  
