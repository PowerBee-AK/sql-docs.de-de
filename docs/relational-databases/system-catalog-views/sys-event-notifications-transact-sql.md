---
description: sys.event_notifications (Transact-SQL)
title: sys.event_notifications (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- event_notifications_TSQL
- event_notifications
- sys.event_notifications_TSQL
- sys.event_notifications
dev_langs:
- TSQL
helpviewer_keywords:
- sys.event_notifications catalog view
ms.assetid: 136a76ee-2b35-4418-ab46-fda2d51f7d99
author: WilliamDAssafMSFT
ms.author: wiassaf
monikerRange: =azuresqldb-current||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: 85f93f5284b8673188d6c6dcb486d80a65d3ccec
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99203870"
---
# <a name="sysevent_notifications-transact-sql"></a>sys.event_notifications (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

  Gibt eine Zeile für jedes Objekt zurück, das eine Ereignis Benachrichtigung ist, mit **sys. Objects. Type** = en.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|Name der Ereignisbenachrichtigung.|  
|**object_id**|**int**|Objekt-ID. Ist innerhalb einer Datenbank eindeutig.|  
|**parent_class**|**tinyint**|Klasse des übergeordneten Objekts.<br /><br /> 0 = Datenbank<br /><br /> 1 = Objekt oder Spalte|  
|**parent_class_desc**|**nvarchar(60)**|DATABASE<br /><br /> OBJECT_OR_COLUMN|  
|**parent_id**|**int**|ID des übergeordneten Objekts ungleich NULL.<br /><br /> 0 = Die übergeordnete Klasse ist die Datenbank.|  
|**create_date**|**datetime**|Erstellungsdatum.|  
|**modify_date**|**datetime**|Ist immer **create_date**.|  
|**service_name**|**nvarchar(256)**|Name des Zieldienstes, an den die Benachrichtigung gesendet wird.|  
|**broker_instance**|**nvarchar(128)**|Broker-Instanz, an den die Benachrichtigung gesendet wird.|  
|**principal_id**|**int**|ID des Datenbankprinzipals, der Besitzer dieser Ereignisbenachrichtigung ist.|  
|**creator_sid**|**varbinary(85)**|SID des Anmeldenamens, der die Ereignisbenachrichtigung erstellt hat.<br /><br /> Ist gleich NULL, wenn die Option FAN_IN nicht angegeben ist.|  
  
## <a name="permissions"></a>Berechtigungen  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Weitere Informationen finden Sie unter [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten für Objekte &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/object-catalog-views-transact-sql.md)   
 [Katalogsichten &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)  
  
  
