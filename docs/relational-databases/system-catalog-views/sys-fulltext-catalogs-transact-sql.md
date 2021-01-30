---
description: sys.fulltext_catalogs (Transact-SQL)
title: sys.fulltext_catalogs (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sys.fulltext_catalogs_TSQL
- sys.fulltext_catalogs
- fulltext_catalogs
- fulltext_catalogs_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.fulltext_catalogs catalog view
ms.assetid: cf1489ff-4819-41fa-a62a-4ed797a16207
author: pmasl
ms.author: pelopes
ms.reviewer: mikeray
ms.openlocfilehash: 38420a12b6b6cab661644ef8d176c6e08c5e0c28
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99191513"
---
# <a name="sysfulltext_catalogs-transact-sql"></a>sys.fulltext_catalogs (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Enthält eine Zeile für jeden Volltextkatalog.  
  
> [!NOTE]  
>  Die folgenden Spalten werden in einer künftigen Version von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]nicht mehr unterstützt: **data_space_id**, **file_id** und **path**. Verwenden Sie diese Spalten nicht für Neuentwicklungen, und planen Sie so bald wie möglich die Änderung von Anwendungen, in denen diese Spalten derzeit verwendet werden.  
 
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|fulltext_catalog_id|**int**|ID des Volltextkatalogs. Diese ID ist innerhalb aller Volltextkataloge in der Datenbank eindeutig.|  
|name|**sysname**|Name des Katalogs. Ist in der Datenbank eindeutig.|  
|path|**nvarchar(260)**|Name des Katalogverzeichnisses im Dateisystem.|  
|is_default|**bit**|Der Standard-Volltextkatalog.<br /><br /> True = Wird als Standard verwendet.<br /><br /> False = Wird nicht als Standard verwendet.|  
|is_accent_sensitivity_on|**bit**|Einstellung des Katalogs für die Unterscheidung nach Akzent.<br /><br /> True = Unterscheidung nach Akzent ist aktiviert.<br /><br /> False = Unterscheidung nach Akzent ist nicht aktiviert.|  
|data_space_id|**int**|Dateigruppe, in der dieser Katalog erstellt wurde.|  
|file_id|**int**|Datei-ID der mit dem Katalog verbundenen Volltextdatei.|  
|principal_id|**int**|ID des Datenbankprinzipals, der den Volltextkatalog besitzt.|  
|is_importing|**bit**|Gibt an, ob der Volltextkatalog importiert wird:<br /><br /> 1 = Der Katalog wird importiert.<br /><br /> 2 = Der Katalog wird nicht importiert.|  
  
## <a name="permissions"></a>Berechtigungen  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)]  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [CREATE FULLTEXT CATALOG &#40;Transact-SQL&#41;](../../t-sql/statements/create-fulltext-catalog-transact-sql.md)   
 [ALTER FULLTEXT CATALOG &#40;Transact-SQL&#41;](../../t-sql/statements/alter-fulltext-catalog-transact-sql.md)   
 [DROP FULLTEXT CATALOG &#40;Transact-SQL&#41;](../../t-sql/statements/drop-fulltext-catalog-transact-sql.md)  
  
  
