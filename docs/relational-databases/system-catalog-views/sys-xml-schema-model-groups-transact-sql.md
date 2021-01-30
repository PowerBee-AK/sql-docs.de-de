---
description: sys.xml_schema_model_groups (Transact-SQL)
title: sys.xml_schema_model_groups (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sys.xml_schema_model_groups
- xml_schema_model_groups
- sys.xml_schema_model_groups_TSQL
- xml_schema_model_groups_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.xml_schema_model_groups catalog view
ms.assetid: 566556dc-a8c8-465c-9196-c7e0ae092a8a
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: 0d2cd070f8e293fc764a996faafab42e8c21a437
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199833"
---
# <a name="sysxml_schema_model_groups-transact-sql"></a>sys.xml_schema_model_groups (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Gibt eine Zeile pro XML-Schemakomponente zurück, die einer Modellgruppe entspricht. Dabei ist **symbol_space** gleich **T**.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**\<inherited columns>**||Erbt Spalten von [sys.xml_schema_components](../../relational-databases/system-catalog-views/sys-xml-schema-components-transact-sql.md).|  
|**compositor**|**char(1)**|Art der compositor-Gruppe:<br /><br /> A = XSD- \<all> Gruppe<br /><br /> C = XSD- \<choice> Gruppe<br /><br /> S = XSD- \<sequence> Gruppe|  
|**compositor_desc**|**nvarchar (60)**|Beschreibung der compositor-Gruppe:<br /><br /> XSD_ALL_GROUP<br /><br /> XSD_CHOICE_GROUP<br /><br /> XSD_SEQUENCE_GROUP|  
  
## <a name="permissions"></a>Berechtigungen  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Weitere Informationen finden Sie unter [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [XML-Schemas &#40;XML-Typsystem&#41; Katalog Sichten &#40;Transact-SQL-&#41;](../../relational-databases/system-catalog-views/xml-schemas-xml-type-system-catalog-views-transact-sql.md)  
  
  
