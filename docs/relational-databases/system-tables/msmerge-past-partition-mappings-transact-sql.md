---
description: MSmerge_past_partition_mappings (Transact-SQL)
title: MSmerge_past_partition_mappings (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSmerge_past_partition_mappings
- MSmerge_past_partition_mappings_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSmerge_past_partition_mappings system table
ms.assetid: 06d54ff5-4d29-4eeb-b8be-64d032e53134
author: cawrites
ms.author: chadam
ms.openlocfilehash: 52b1099fb1cfcda5f61f9e9d0085e955aea72247
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205945"
---
# <a name="msmerge_past_partition_mappings-transact-sql"></a>MSmerge_past_partition_mappings (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  In der **MSmerge_past_partition_mappings** Tabelle wird eine Zeile für jede Partitions-ID gespeichert, für die eine bestimmte geänderte Zeile verwendet wurde, die nicht mehr zu gehört. Diese Tabelle wird in der Veröffentlichungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**publication_number**|**smallint**|Die Veröffentlichungsnummer, die in **sysmergepublications** gespeichert wird.|  
|**tablenick**|**int**|Der Spitzname der veröffentlichten Tabelle.|  
|**ROWGUID**|**uniqueidentifier**|Der Zeilenbezeichner für die angegebene Zeile.|  
|**partition_id**|**int**|Die Partitions-ID, die der Zeile zugeordnet ist. Der Wert ist-1, wenn die Zeilen Änderung für alle Abonnenten relevant ist.|  
|**Stro**|**bigint**|Der Wert der Generierung, in der die Partitionsänderung aufgetreten ist.|  
|**reason**|**tinyint**|Nur intern verwendet.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
