---
description: MSsnapshot_history (Transact-SQL)
title: MSsnapshot_history (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSsnapshot_history
- MSsnapshot_history_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSsnapshot_history system table
ms.assetid: 56bf4128-1689-4963-9343-432dd0898d31
author: cawrites
ms.author: chadam
ms.openlocfilehash: 246c0baa64c13b5695964251b6703bae31c5bd49
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199051"
---
# <a name="mssnapshot_history-transact-sql"></a>MSsnapshot_history (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MSsnapshot_history** Tabelle enthält Verlaufs Zeilen für die dem lokalen Verteiler zugeordneten Momentaufnahme-Agents. Diese Tabelle wird in der Verteilungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**agent_id**|**int**|Die ID des Momentaufnahme-Agents.|  
|**RunStatus**|**int**|Der Ausführungsstatus:<br /><br /> **1** = Start.<br /><br /> **2** = erfolgreich.<br /><br /> **3** = wird ausgeführt.<br /><br /> **4** = im Leerlauf.<br /><br /> **5** = Wiederholungsversuch.<br /><br /> **6** = Fehler.|  
|**start_time**|**datetime**|Der Zeitpunkt, zu dem mit der Ausführung des Auftrags begonnen wird.|  
|**time**|**datetime**|Der Zeitpunkt der Protokollierung der Meldung.|  
|**duration**|**int**|Die Dauer der Meldungssitzung in Sekunden.|  
|**Kommentare**|**nvarchar(255)**|Der Meldungstext.|  
|**delivered_transactions**|**int**|Die Gesamtzahl der in der Sitzung übermittelten Transaktionen.|  
|**delivered_commands**|**int**|Die Anzahl der pro Sekunde übermittelten Befehle.|  
|**delivery_rate**|**float(53)**|Die durchschnittliche Anzahl der pro Sekunde übermittelten Befehle.|  
|**error_id**|**int**|Die ID des Fehlers in der [MSrepl_errors](../../relational-databases/system-tables/msrepl-errors-transact-sql.md) -Systemtabelle.|  
|**timestamp**|**timestamp**|Die Timestampspalte dieser Tabelle.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
