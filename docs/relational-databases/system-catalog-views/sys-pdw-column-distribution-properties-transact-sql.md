---
description: sys.pdw_column_distribution_properties (Transact-SQL)
title: sys.pdw_column_distribution_properties (Transact-SQL)
ms.custom: seo-dt-2019
ms.date: 03/03/2017
ms.prod: sql
ms.technology: data-warehouse
ms.reviewer: ''
ms.topic: reference
dev_langs:
- TSQL
ms.assetid: 46b74f99-2e22-4dbd-872a-533fce0e239c
author: ronortloff
ms.author: rortloff
monikerRange: '>= aps-pdw-2016 || = azure-sqldw-latest'
ms.openlocfilehash: d812be285cb2a89aaa6f83db2d08312dfed939af
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99191219"
---
# <a name="syspdw_column_distribution_properties-transact-sql"></a>sys.pdw_column_distribution_properties (Transact-SQL)
[!INCLUDE[applies-to-version/asa-pdw](../../includes/applies-to-version/asa-pdw.md)]

  Enthält Verteilungs Informationen für Spalten.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|Range|  
|-----------------|---------------|-----------------|-----------|  
|**object_id**|**int**|ID des Objekts, zu dem die Spalte gehört.||  
|**column_id**|**int**|ID der Spalte.||  
|**distribution_ordinal**|**tinyint**|Ordinalzahl (1-basiert) innerhalb des Satzes der Verteilung.|0 = keine Verteilungs Spalte. 1 = [!INCLUDE[ssSDW](../../includes/sssdw-md.md)] verwendet diese Spalte, um die übergeordnete Tabelle zu verteilen.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten von Azure Synapse Analytics und Parallel Data Warehouse Catalog](../../relational-databases/system-catalog-views/sql-data-warehouse-and-parallel-data-warehouse-catalog-views.md)  
  
  
