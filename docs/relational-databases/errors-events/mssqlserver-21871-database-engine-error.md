---
description: MSSQLSERVER_21871
title: MSSQLSERVER_21871 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 21871 (Database Engine error)
ms.assetid: d3215378-9282-444f-a18b-00b96fd0133d
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 1085b9ad233df60e39dca019bd9cf7b1e424942f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99196417"
---
# <a name="mssqlserver_21871"></a>MSSQLSERVER_21871
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|21871|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|SQLErrorNum21871|  
|Meldungstext|Verleger %s der Datenbank %s wurde nicht umgeleitet.|  
  
## <a name="explanation"></a>Erklärung  
**sp_validate_replica_hosts_as_publishers** überprüft die Tabelle MSredirected_publishers in der Verteilungsdatenbank auf einen Eintrag für den identifizierten Verleger und die Verlegerdatenbank.  **sp_validate_replica_hosts_as_publishers** gibt den Fehler 21871 zurück, wenn kein Eintrag gefunden wird.  
  
## <a name="user-action"></a>Benutzeraktion  
**sp_validate_replica_hosts_as_publishers** ist nur für umgeleitete Verleger relevant. Wenn eine veröffentlichte Datenbank Mitglied einer Always On-Verfügbarkeitsgruppe ist, führen Sie die gespeicherte Prozedur **sp_redirect_publisher** aus, um den Verleger und die Verlegerdatenbank mit dem Verfügbarkeitsgruppen-Listener-Namen der Verfügbarkeitsgruppe zu verknüpfen.  
  
