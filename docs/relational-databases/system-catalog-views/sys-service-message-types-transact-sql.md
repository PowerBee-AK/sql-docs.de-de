---
description: sys.service_message_types (Transact-SQL)
title: sys.service_message_types (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sys.service_message_types
- service_message_types
- sys.service_message_types_TSQL
- service_message_types_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.service_message_types catalog view
ms.assetid: 6a38709a-60fe-46f6-89da-718f74f15600
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: 9ce8898f707a1c82f98e88a04f52ffd706cd7fb4
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99204497"
---
# <a name="sysservice_message_types-transact-sql"></a>sys.service_message_types (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Diese Katalogsicht enthält eine Zeile pro Nachrichtentyp, der im Service Broker registriert ist.
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|Der Name des Nachrichtentypes, der innerhalb der Datenbank eindeutig ist. Lässt keine NULL-Werte zu.|  
|**message_type_id**|**int**|Die ID des Nachrichtentypes, die innerhalb der Datenbank eindeutig ist. Lässt keine NULL-Werte zu.|  
|**principal_id**|**int**|Die ID des Datenbankprinzipals, der diesen Nachrichtentyp besitzt. Lässt NULL-Werte zu.|  
|**validation**|**char(2)**|Vom Broker vor dem Senden von Nachrichten dieses Types ausgeführte Überprüfung. Lässt keine NULL-Werte zu. Enthält einen der folgenden Werte:<br /><br /> N = Keiner<br /><br /> X = XML<br /><br /> E = Leer|  
|**validation_desc**|**nvarchar(60)**|Beschreibung der vom Broker vor dem Senden von Nachrichten dieses Types ausgeführten Überprüfung. Lässt NULL-Werte zu. Enthält einen der folgenden Werte:<br /><br /> Keine<br /><br /> XML<br /><br /> EMPTY|  
|**xml_collection_id**|**int**|Für eine Überprüfung, die ein XML-Schema verwendet, wird die ID der Schemaauflistung verwendet.<br /><br /> Andernfalls wird NULL verwendet.|  
  
## <a name="permissions"></a>Berechtigungen  
 [!INCLUDE[ssCatViewPerm](../../includes/sscatviewperm-md.md)] Weitere Informationen finden Sie unter [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).  
  
  
