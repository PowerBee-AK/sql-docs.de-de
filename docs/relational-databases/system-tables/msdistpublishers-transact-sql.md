---
description: MSdistpublishers (Transact-SQL)
title: MSdistpublishers (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSdistpublishers
- MSdistpublishers_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSdistpublishers system table
ms.assetid: 31844099-4b33-4dc9-84b4-bac70aa82598
author: cawrites
ms.author: chadam
ms.openlocfilehash: cfb8cfe834006d0d23ca0ed41959d73351208c25
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99160431"
---
# <a name="msdistpublishers-transact-sql"></a>MSdistpublishers (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  Die **MSdistpublishers** -Tabelle enthält eine Zeile für jeden Remote Verleger, der vom lokalen Verteiler unterstützt wird. Diese Tabelle wird in der **msdb** -Datenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**name**|**sysname**|Der Name des Verlegerverteilers.|  
|**distribution_db**|**sysname**|Der Name der Verteilungs Datenbank.|  
|**working_directory**|**nvarchar(255)**|Der Name des Arbeitsverzeichnisses, das zum Speichern von Daten-und Schema Dateien für die Veröffentlichung verwendet wird.|  
|**security_mode**|**int**|Der auf dem Verteiler implementierte Sicherheitsmodus:<br /><br /> **0** -  =  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Authentifizierung.<br /><br /> **1** = Windows-Authentifizierung.|  
|**Anmel**|**sysname**|Die Anmelde-ID für die [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Authentifizierung.|  
|**password**|**nvarchar (524)**|Das (verschlüsselte) Kennwort für die [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Authentifizierung.|  
|**active**|**bit**|Zeigt an, ob der lokale Verteiler zurzeit vom Remoteverleger verwendet wird.|  
|**trusted**|**bit**|Zeigt an, ob auf dem Remoteverleger dasselbe Kennwort wie auf dem lokalen Verteiler verwendet wird:<br /><br /> **0** = auf dem Remote Verleger ist ein Kennwort erforderlich, um eine Verbindung mit dem Verteiler herzustellen.<br /><br /> **1** = es ist kein Kennwort erforderlich.|  
|**third_party**|**bit**|Gibt an, ob es sich bei dem Verleger um eine [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Installation handelt:<br /><br /> **0** -  =  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Installation **. 1** = heterogene Datenquelle.|  
|**publisher_type**|**sysname**|Der Typ des Verlegers:<br /><br /> **MSSQLSERVER**  =  [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Gebers.<br /><br /> **Oracle** = Standard-Oracle-Verleger.<br /><br /> **Oracle Gateway** = Oracle-Gatewayverleger.|  
|**storage_connection_string**|**nvarchar (779)**|Wert der Verbindungs Zeichenfolge für Azure SQL-Daten Bank Speicher.|  

  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
