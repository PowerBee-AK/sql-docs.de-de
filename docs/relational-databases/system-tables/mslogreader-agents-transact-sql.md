---
description: MSlogreader_agents (Transact-SQL)
title: MSlogreader_agents (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSlogreader_agents_TSQL
- MSlogreader_agents
dev_langs:
- TSQL
helpviewer_keywords:
- MSlogreader_agents system table
ms.assetid: 8baa3c5a-cb40-42d0-b966-00e6d55368e8
author: cawrites
ms.author: chadam
ms.openlocfilehash: cbf7f439c03ff29e205b7a19a159b67b43090a71
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99212314"
---
# <a name="mslogreader_agents-transact-sql"></a>MSlogreader_agents (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MSlogreader_agents** Tabelle enthält eine Zeile für jede Protokolllese-Agent, die auf dem lokalen Verteiler ausgeführt wird. Diese Tabelle wird in der Verteilungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**id**|**int**|Die ID des Protokolllese-Agents.|  
|**name**|**nvarchar (100)**|Der Name des Protokolllese-Agents|  
|**publisher_id**|**smallint**|Die ID des Verlegers|  
|**publisher_db**|**sysname**|Der Name der Verlegerdatenbank.|  
|**ung**|**sysname**|Der Name der Veröffentlichung.|  
|**local_job**|**bit**|Gibt an, ob sich ein [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Agent-Auftrag auf dem lokalen Verteiler befindet.|  
|**job_id**|**Binary (16)**|Die Auftrags-ID|  
|**profile_id**|**int**|Die Konfigurations-ID aus der [MSagent_profiles](../../relational-databases/system-tables/msagent-profiles-transact-sql.md) Tabelle.|  
|**publisher_security_mode**|**smallint**|Der Sicherheitsmodus, der vom Agent beim Herstellen einer Verbindung mit dem Verleger verwendet wird. Dies kann einer der folgenden Modi sein:<br /><br /> **0** -  =  [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Authentifizierung.<br /><br /> **1**  =  [!INCLUDE[msCoName](../../includes/msconame-md.md)] Windows-Authentifizierung.|  
|**publisher_login**|**sysname**|Der Anmeldename, der beim Herstellen einer Verbindung mit dem Verleger verwendet wird|  
|**publisher_password**|**nvarchar (524)**|Der verschlüsselte Wert des Kennworts, das verwendet wird, um eine Verbindung mit dem Verleger herzustellen.|  
|**job_step_uid**|**uniqueidentifier**|Die eindeutige ID des Auftragsschritts des [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Agents, in dem der Agent gestartet wird.|  
|**job_login**|**sysname**||  
|**job_password**|**nvarchar (524)**||  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
