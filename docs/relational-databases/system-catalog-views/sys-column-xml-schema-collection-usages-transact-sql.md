---
description: sys.column_xml_schema_collection_usages (Transact-SQL)
title: sys.column_xml_schema_collection_usages (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- column_xml_schema_collection_usages_TSQL
- sys.column_xml_schema_collection_usages
- column_xml_schema_collection_usages
- sys.column_xml_schema_collection_usages_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.column_xml_schema_collection_usages catalog view
ms.assetid: 4fd1ec7f-b9dc-4ddb-ab3a-0d59ab05ad20
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: bcc015f19b1bc9d9bffce3d488bcbf6369c96a28
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99190889"
---
# <a name="syscolumn_xml_schema_collection_usages-transact-sql"></a>sys.column_xml_schema_collection_usages (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Gibt eine Zeile für jede Spalte zurück, die durch ein XML-Schema überprüft wird.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**object_id**|**int**|Die ID des Objekts, zu dem diese Spalte gehört.|  
|**column_id**|**int**|Die ID der Spalte. Ist eindeutig innerhalb des Objekts.|  
|**xml_collection_id**|**int**|Die ID der Auflistung, die den überprüfenden XML-Schemanamespace der Spalte enthält.|  
  
## <a name="permissions"></a>Berechtigungen  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Weitere Informationen finden Sie unter [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [XML-Schemas &#40;XML-Typsystem&#41; Katalog Sichten &#40;Transact-SQL-&#41;](../../relational-databases/system-catalog-views/xml-schemas-xml-type-system-catalog-views-transact-sql.md)  
  
  
