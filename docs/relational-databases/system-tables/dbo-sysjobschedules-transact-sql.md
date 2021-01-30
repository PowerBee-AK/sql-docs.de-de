---
description: dbo.sysjobschedules (Transact-SQL)
title: dbo.sysjobzeitpläne (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 08/09/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sysjobschedules
- dbo.sysjobschedules
- dbo.sysjobschedules_TSQL
- sysjobschedules_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sysjobschedules system table
ms.assetid: ccdafec7-2a9b-4356-bffb-1caa3a12db59
author: cawrites
ms.author: chadam
ms.openlocfilehash: f82fae854a00e73ec7d8d45304ee486e0df33373
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99160002"
---
# <a name="dbosysjobschedules-transact-sql"></a>dbo.sysjobschedules (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Enthält Zeitplaninformationen für Aufträge, die vom [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Agent ausgeführt werden sollen. Diese Tabelle wird in der **msdb** -Datenbank gespeichert.  
  
> **Hinweis:** Die **sysjobzeitpläne** -Tabelle wird alle 20 Minuten aktualisiert, was sich auf die Werte auswirken kann, die von der gespeicherten Prozedur **sp_help_jobschedule** zurückgegeben werden.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**schedule_id**|**int**|ID des Zeitplans.|  
|**job_id**|**uniqueidentifier**|ID des Auftrags.|  
|**next_run_date**|**int**|Das nächste Datum, an dem eine Ausführung des Auftrags geplant ist. Für das Datum wird das Format YYYYMMDD verwendet.|  
|**next_run_time**|**int**|Uhrzeit, an der eine Ausführung des Auftrags geplant ist. Für die Uhrzeit wird das Format HHMMSS und eine 24-Stunden-Schreibweise verwendet.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [dbo.sysZeitpläne &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/dbo-sysschedules-transact-sql.md)  
  
  
