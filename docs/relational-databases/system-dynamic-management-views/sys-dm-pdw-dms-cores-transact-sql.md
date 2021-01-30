---
description: sys.dm_pdw_dms_cores (Transact-SQL)
title: sys.dm_pdw_dms_cores (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/07/2017
ms.prod: sql
ms.technology: data-warehouse
ms.reviewer: ''
ms.topic: reference
dev_langs:
- TSQL
ms.assetid: b3f09b15-0863-4418-9347-a4f5fd2ab7c7
author: ronortloff
ms.author: rortloff
monikerRange: '>= aps-pdw-2016 || = azure-sqldw-latest'
ms.openlocfilehash: 29431a3e38ff15b63f40ab1d18269337d55cdd49
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99143742"
---
# <a name="sysdm_pdw_dms_cores-transact-sql"></a>sys.dm_pdw_dms_cores (Transact-SQL)
[!INCLUDE[applies-to-version/asa-pdw](../../includes/applies-to-version/asa-pdw.md)]

  Enthält Informationen zu allen DMS-Diensten, die auf den Computeknoten des Geräts ausgeführt werden. Sie listet eine Zeile pro Dienst Instanz auf, die derzeit eine Zeile pro Knoten ist.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|Range|  
|-----------------|---------------|-----------------|-----------|  
|dms_core_id|**int**|Eindeutige numerische ID, die diesem DMS-Kern zugeordnet ist.<br /><br /> Der Schlüssel für diese Ansicht.|Legen Sie auf den pdw_node_id des Knotens fest, auf dem dieser DMS-Kern ausgeführt wird.|  
|pdw_node_id|**int**|ID des Knotens, auf dem dieser DMS-Dienst ausgeführt wird.|Weitere Informationen finden Sie unter node_id in [sys.dm_pdw_nodes &#40;Transact-SQL-&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-pdw-nodes-transact-sql.md).|  
|status|**nvarchar(32)**|Aktueller Status des DMS-Dienstanbieter.|[!INCLUDE[ssInfoNA](../../includes/ssinfona-md.md)]|  
  
 Informationen über die maximale Anzahl von Zeilen, die in dieser Sicht beibehalten werden, finden Sie im Abschnitt "Metadaten" im Thema [Kapazitäts Limits](/azure/sql-data-warehouse/sql-data-warehouse-service-capacity-limits#metadata) .  
  
## <a name="see-also"></a>Weitere Informationen  
 [Azure Synapse Analytics und parallele Data Warehouse dynamische Verwaltungs Sichten &#40;Transact-SQL-&#41;](../../relational-databases/system-dynamic-management-views/sql-and-parallel-data-warehouse-dynamic-management-views.md)  
  
  
