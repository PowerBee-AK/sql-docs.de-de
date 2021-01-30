---
description: sys.sysoledbusers (Transact-SQL)
title: sys.sysoledbusers (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/15/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sys.sysoledbusers
- sys.sysoledbusers_TSQL
- sysoledbusers
- sysoledbusers_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sysoledbusers system table
- sys.sysoledbusers compatibility view
ms.assetid: fe924c17-9cad-4b2b-8124-1e0fd82931e3
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: 4e8c134ad74b24704696b586bb362ab253dedb84
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99148534"
---
# <a name="syssysoledbusers-transact-sql"></a>sys.sysoledbusers (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

    
> [!IMPORTANT]  
>  Diese [!INCLUDE[ssVersion2000](../../includes/ssversion2000-md.md)]-Systemtabelle wird nur aus Gründen der Abwärtskompatibilität als Sicht in [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] bereitgestellt. Es wird empfohlen, stattdessen [Katalog Sichten](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md) zu verwenden.  
  
 Enthält eine Zeile für jede Benutzer- und Kennwortzuordnung für den angegebenen Verbindungsserver. **sysoledbusers** wird in der **Master** -Datenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**rmtsrvid**|**smallint**|Sicherheits-ID (SID) des Servers.|  
|**rmtloginame**|**nvarchar (** 128 **)**|Der Name des Remote Anmelde namens, dem **LoginSID** für die verknüpfte **rmtservid** zugeordnet ist.|  
|**rmtpassword**|**nvarchar (** 128 **)**|Gibt NULL zurück.|  
|**LoginSID**|**varbinary (** 85 **)**|SID des lokalen Anmeldenamens, der zugeordnet werden soll.|  
|**status**|**smallint**|Wenn 1, sollten die Anmeldeinformationen des Benutzers für die Zuordnung verwendet werden.|  
|**changedate**|**datetime**|Datum, an dem die Zuordnungsinformationen zuletzt geändert wurden.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Katalogsichten &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [Kompatibilitätssichten &#40;Transact-SQL&#41;](~/relational-databases/system-compatibility-views/system-compatibility-views-transact-sql.md)  
  
  
