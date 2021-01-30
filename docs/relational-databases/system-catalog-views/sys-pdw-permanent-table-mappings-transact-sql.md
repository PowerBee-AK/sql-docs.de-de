---
title: sys.pdw_permanent_table_mappings (Transact-SQL)
ms.custom: ''
ms.date: 07/24/2020
ms.prod: sql
ms.technology: data-warehouse
ms.reviewer: ''
ms.topic: reference
dev_langs:
- TSQL
author: mstehrani
ms.author: emtehran
monikerRange: = azure-sqldw-latest
ms.openlocfilehash: 1258a6131ccd0ad2280066faef6ac966bb0fb4d5
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99212059"
---
# <a name="syspdw_permanent_table_mappings-transact-sql"></a>sys.pdw_permanent_table_mappings (Transact-SQL)
[!INCLUDE [applies-to-version/asa](../../includes/applies-to-version/asa.md)]

  Bindet permanente Benutzer Tabellen mit internen Objektnamen **object_id**.  
  
> [!NOTE]
> **sys.pdw_permanent_table_mappings** enthält Zuordnungen zu permanenten Tabellen und schließt keine temporären oder externen Tabellen Zuordnungen ein.

|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|physical_name|**nvarchar (36)**|Der physische Name für die Tabelle.<br /><br /> **physical_name** und **object_id** den Schlüssel für diese Ansicht bilden.||  
|object_id|**int**|Die Objekt-ID für die Tabelle. Weitere Informationen finden Sie unter [sys. Objects &#40;Transact-SQL-&#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md).<br /><br /> **physical_name** und **object_id** den Schlüssel für diese Ansicht bilden.||  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten von Azure Synapse Analytics und Parallel Data Warehouse Catalog](../../relational-databases/system-catalog-views/sql-data-warehouse-and-parallel-data-warehouse-catalog-views.md)   
 [sys.pdw_index_mappings &#40;Transact-SQL-&#41;](../../relational-databases/system-catalog-views/sys-pdw-index-mappings-transact-sql.md)  
  
  
