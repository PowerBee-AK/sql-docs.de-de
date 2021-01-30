---
description: sys.pdw_materialized_view_column_distribution_properties (Transact-SQL)
title: sys.pdw_materialized_view_column_distribution_properties (Transact-SQL)
ms.custom: seo-dt-2019
ms.date: 07/03/2019
ms.prod: sql
ms.technology: data-warehouse
ms.reviewer: jrasnick
ms.topic: reference
dev_langs:
- TSQL
ms.assetid: d62b0e25-3226-4f87-a10a-b3a0d9555e19
author: XiaoyuMSFT
ms.author: xiaoyul
monikerRange: = azure-sqldw-latest
ms.openlocfilehash: 6f6bb814bd35728824e790a5b11e6fe7ca6f65fa
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99204824"
---
# <a name="syspdw_materialized_view_column_distribution_properties-transact-sql"></a>sys.pdw_materialized_view_column_distribution_properties (Transact-SQL) 

[!INCLUDE [asa](../../includes/applies-to-version/asa.md)]

Zeigt Verteilungs Informationen für Spalten in einer materialisierten Sicht an.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|object_id|**int**|ID des Objekts, zu dem die Spalte gehört. |  
|column_id|**int**|Die ID der Spalte.|  
|distribution_ordinal|**tinyint**|0 = keine Verteilungs Spalte.</br> 1 = Azure Synapse Analytics verwendet diese Spalte, um die materialisierte Sicht zu verteilen.|
 
## <a name="permissions"></a>Berechtigungen 

Erfordert die VIEW DATABASE STATE-Berechtigung.

## <a name="see-also"></a>Weitere Informationen

[Leistungsoptimierung durch materialisierte Sicht](/azure/sql-data-warehouse/performance-tuning-materialized-views)   
[CREATE MATERIALIZED VIEW AS SELECT &#40;Transact-SQL&#41;](../../t-sql/statements/create-materialized-view-as-select-transact-sql.md?view=azure-sqldw-latest&preserve-view=true)   
[ALTER MATERIALIZED VIEW &#40;Transact-SQL&#41;](../../t-sql/statements/alter-materialized-view-transact-sql.md?view=azure-sqldw-latest&preserve-view=true)   
[EXPLAIN &#40;Transact-SQL&#41;](../../t-sql/queries/explain-transact-sql.md?view=azure-sqldw-latest&preserve-view=true)   
[sys.pdw_materialized_view_distribution_properties &#40;Transact-SQL&#41;](./sys-pdw-materialized-view-distribution-properties-transact-sql.md?view=azure-sqldw-latest&preserve-view=true)   
[sys.pdw_materialized_view_mappings &#40;Transact-SQL&#41;](./sys-pdw-materialized-view-mappings-transact-sql.md?view=azure-sqldw-latest&preserve-view=true)   
[DBCC PDW_SHOWMATERIALIZEDVIEWOVERHEAD &#40;Transact-SQL&#41;](../../t-sql/database-console-commands/dbcc-pdw-showmaterializedviewoverhead-transact-sql.md?view=azure-sqldw-latest&preserve-view=true)   
[Katalogsichten von Azure Synapse Analytics und Parallel Data Warehouse Catalog](../../relational-databases/system-catalog-views/sql-data-warehouse-and-parallel-data-warehouse-catalog-views.md)   
[In Azure Synapse Analytics unterstützte Systemsichten](/azure/sql-data-warehouse/sql-data-warehouse-reference-tsql-system-views)   
[In Azure Synapse Analytics unterstützte T-SQL-Anweisungen](/azure/sql-data-warehouse/sql-data-warehouse-reference-tsql-statements)