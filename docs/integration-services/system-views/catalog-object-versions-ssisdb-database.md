---
description: catalog.object_versions (SSISDB-Datenbank)
title: catalog.object_versions (SSISDB-Datenbank) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: language-reference
ms.assetid: 2fd8c020-1c77-4702-8e6b-efa6a348daab
author: chugugrace
ms.author: chugu
ms.openlocfilehash: 83ccc09b8a38340939340f214c3ca62fddca6d47
ms.sourcegitcommit: 868c60aa3a76569faedd9b53187e6b3be4997cc9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2021
ms.locfileid: "99835160"
---
# <a name="catalogobject_versions-ssisdb-database"></a>catalog.object_versions (SSISDB-Datenbank)

[!INCLUDE[sqlserver-ssis](../../includes/applies-to-version/sqlserver-ssis.md)]

  Zeigt die Versionen von Objekten im [!INCLUDE[ssISnoversion](../../includes/ssisnoversion-md.md)] -Katalog an. In dieser Version werden in dieser Sicht nur Versionen von Projekten unterstützt.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|object_version_lsn|**bigint**|Der eindeutige Bezeichner (ID) der Objektversion. Diese Nummer ist nicht unbedingt eine fortlaufende Nummer.|  
|object_id|**bigint**|Die eindeutige ID des Objekts.|  
|object_type|**smallint**|Der Objekttyp. Der Wert `20` wird für Projekte angezeigt.|  
|object_name|**sysname(nvarchar(128))**|Der Name des Objekts.|  
|description|**nvarchar(1024)**|Die Beschreibung des Projekts.|  
|created_by|**nvarchar(128)**|Der Name des Benutzers, der dem Katalog das Objekt hinzugefügt hat.|  
|created_time|**datetimeoffset**|Datum und Uhrzeit, zu denen dem Katalog das Objekt hinzugefügt wurde.|  
|restored_by|**nvarchar(128)**|Der Name des Benutzers, der das Objekt wiederhergestellt hat.|  
|last_restored_time|**datetimeoffset**|Datum und Uhrzeit, zu denen das Objekt zuletzt wiederhergestellt wurde.|  
  
## <a name="remarks"></a>Hinweise  
 In dieser Sicht wird eine Zeile für jede Version eines Objekts im Katalog angezeigt.  
  
## <a name="permissions"></a>Berechtigungen  
 Zum Anzeigen von Zeilen in dieser Sicht benötigten Sie eine der folgenden Berechtigungen:  
  
-   READ-Berechtigung für das Objekt  
  
-   Mitgliedschaft in der Datenbankrolle **ssis_admin**  
  
-   Mitgliedschaft in der Serverrolle **sysadmin**  
  
> [!NOTE]  
>  Sicherheit auf Zeilenebene wird erzwungen. Es werden nur Zeilen angezeigt, zu deren Anzeige Sie berechtigt sind.  
  
  
