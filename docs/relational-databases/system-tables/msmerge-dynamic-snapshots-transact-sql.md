---
description: MSmerge_dynamic_snapshots (Transact-SQL)
title: MSmerge_dynamic_snapshots (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSmerge_dynamic_snapshots_TSQL
- MSmerge_dynamic_snapshots
dev_langs:
- TSQL
helpviewer_keywords:
- MSmerge_dynamic_snapshots system table
ms.assetid: a5592b3c-731b-4fc9-ae4b-2602ed78248e
author: cawrites
ms.author: chadam
ms.openlocfilehash: 0bea9259e6218d32ae0e278046493aaeeafeaa41
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99181263"
---
# <a name="msmerge_dynamic_snapshots-transact-sql"></a>MSmerge_dynamic_snapshots (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  In der **MSmerge_dynamic_snapshots** Tabelle wird der Speicherort der gefilterten Daten Momentaufnahme für jede Partition nachverfolgt, die für eine Mergeveröffentlichung mit parametrisierten Zeilen filtern definiert ist. Diese Tabelle wird in der **Veröffentlichungs** Datenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**partition_id**|**int**|Die ID der Mergepartition.|  
|**dynamic_snapshot_location**|**nvarchar(255)**|Der Standort der gefilterten Datenmomentaufnahme für die Partition.|  
|**last_updated**|**datetime**|Das Datum, an dem die gefilterte Datenmomentaufnahme aktualisiert wurde.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikationstabellen &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)  
  
  
