---
description: sys.dm_pdw_sys_info (Transact-SQL)
title: sys.dm_pdw_sys_info (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/07/2017
ms.prod: sql
ms.technology: data-warehouse
ms.reviewer: ''
ms.topic: reference
dev_langs:
- TSQL
ms.assetid: 686976b4-2d5d-4d64-bf12-56eba1dc59b1
author: ronortloff
ms.author: rortloff
monikerRange: '>= aps-pdw-2016 || = azure-sqldw-latest'
ms.openlocfilehash: 7d69c8c58f46d6fbbccc5ee98ead54f222b5e2a9
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99139080"
---
# <a name="sysdm_pdw_sys_info-transact-sql"></a>sys.dm_pdw_sys_info (Transact-SQL)
[!INCLUDE[applies-to-version/asa-pdw](../../includes/applies-to-version/asa-pdw.md)]

  Stellt einen Satz von Leistungsindikatoren auf Geräteebene bereit, die die Gesamtaktivität auf der Appliance widerspiegeln.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|Range|  
|-----------------|---------------|-----------------|-----------|  
|total_sessions|**int**|Anzahl von Sitzungen, die sich derzeit im System befinden.|0 bis max_active_sessions (siehe unten).|  
|idle_sessions|**int**|Anzahl der derzeit im Leerlauf befindlichen Sitzungen.||  
|active_requests|**int**|Anzahl der aktiven Anforderungen, die zurzeit ausgeführt werden.||  
|queued_requests|**int**|Anzahl der zurzeit in der Warteschlange eingereihten Anforderungen.||  
|active_loads|**int**|Anzahl der Ladevorgänge, die derzeit im System ausgeführt werden.||  
|queued_loads|**int**|Anzahl der in der Warteschlange befindlichen Ladungen, die auf die Ausführung warten||  
|active_backups|**int**|Anzahl der zurzeit laufenden Sicherungen.||  
|active_restores|**int**|Anzahl der zurzeit laufenden Sicherungs Wiederherstellungen.||  
  
## <a name="see-also"></a>Weitere Informationen  
 [Azure Synapse Analytics und parallele Data Warehouse dynamische Verwaltungs Sichten &#40;Transact-SQL-&#41;](../../relational-databases/system-dynamic-management-views/sql-and-parallel-data-warehouse-dynamic-management-views.md)  
  
  
