---
description: dbo.systaskids (Transact-SQL)
title: dbo.sysTaskIDs (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 08/09/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- systaskids_TSQL
- dbo.systaskids
- systaskids
- dbo.systaskids_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- systaskids system table
ms.assetid: 45c56d89-4160-4d84-80bf-a7a05488792d
author: cawrites
ms.author: chadam
ms.openlocfilehash: 56e60ac3644eb9523b082a0f0665fbefbe99da60
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99207243"
---
# <a name="dbosystaskids-transact-sql"></a>dbo.systaskids (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Enthält eine Zuordnung von in früheren Versionen von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] erstellten Tasks zu [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)] -Aufträgen in der aktuellen Version. Diese Tabelle wird in der **msdb** -Datenbank gespeichert.  
  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**task_id**|**int**|ID des Tasks.|  
|**job_id**|**uniqueidentifier**|ID des Auftrags, dem der Task zugeordnet ist.|  
  
  
