---
description: sys.dm_pdw_os_performance_counters (Transact-SQL)
title: sys.dm_pdw_os_performance_counters (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/07/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
dev_langs:
- TSQL
ms.assetid: 0673a8f8-8bed-41eb-8959-a9e3e9e03a65
author: WilliamDAssafMSFT
ms.author: wiassaf
monikerRange: '>= aps-pdw-2016'
ms.openlocfilehash: ea7840aa8514bd3bdbc03004e551c66ad01944fb
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99140141"
---
# <a name="sysdm_pdw_os_performance_counters-transact-sql"></a>sys.dm_pdw_os_performance_counters (Transact-SQL)
[!INCLUDE [pdw](../../includes/applies-to-version/pdw.md)]

  Enthält Informationen zu den Windows-Leistungsindikatoren für die Knoten in [!INCLUDE[ssPDW](../../includes/sspdw-md.md)] .  
  
|Spaltenname|Datentyp|BESCHREIBUNG|Range|  
|-----------------|---------------|-----------------|-----------|  
|pdw_node_id|**int**|Die ID des Knotens, der den Zählers enthält.<br /><br /> pdw_node_id und counter_name den Schlüssel für diese Ansicht bilden.|Weitere Informationen finden Sie unter node_id in [sys.dm_pdw_nodes &#40;Transact-SQL-&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-pdw-nodes-transact-sql.md).|  
|counter_name|**nvarchar(255)**|Der Name des Windows-Leistungs Zählers.||  
|counter_category|**nvarchar(255)**|Der Name der Windows-Leistungs Leistungswert Kategorie.||  
|instance_name|**nvarchar(255)**|Name der spezifischen Instanz des Leistungsindikators.||  
|counter_value|**Decimal (38, 10)**|Aktueller Wert des Leistungsindikators.||  
|last_update_time|**Datetime2 (3)**|Zeitstempel des letzten Updates des Werts.||  
  
## <a name="see-also"></a>Weitere Informationen  
 [Azure Synapse Analytics und parallele Data Warehouse dynamische Verwaltungs Sichten &#40;Transact-SQL-&#41;](../../relational-databases/system-dynamic-management-views/sql-and-parallel-data-warehouse-dynamic-management-views.md)  
  
  
