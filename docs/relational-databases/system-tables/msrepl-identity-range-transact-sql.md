---
description: MSrepl_identity_range (Transact-SQL)
title: MSrepl_identity_range (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSrepl_identity_range_TSQL
- MSrepl_identity_range
dev_langs:
- TSQL
helpviewer_keywords:
- MSrepl_identity_range system table
ms.assetid: 6e92a8e8-7667-4c98-b1c4-46735bac50d8
author: cawrites
ms.author: chadam
ms.openlocfilehash: f2608a2012f22fa8db8fdbab1b982e77aacf8e0a
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99179168"
---
# <a name="msrepl_identity_range-transact-sql"></a>MSrepl_identity_range (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MSrepl_identity_range** Tabelle bietet Unterstützung für die Identitäts Bereichs Verwaltung. Diese Tabelle wird in den Datenbanken publication, distribution und subscription gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**publisher**|**sysname**|Der Name des Verlegers.|  
|**publisher_db**|**sysname**|Der Name der Veröffentlichungs Datenbank.|  
|**TableName**|**sysname**|Der Name der Tabelle.|  
|**identity_support**|**int**|Gibt an, ob die automatische Behandlung der Identitätsbereiche aktiviert ist. 0 gibt an, dass die automatische Behandlung der Identitätsbereiche nicht aktiviert ist.|  
|**next_seed**|**bigint**|Wenn die automatische Behandlung der Identitätsbereiche aktiviert ist, zeigt dieser Wert den Anfangspunkt des nächsten Bereichs an.|  
|**pub_range**|**bigint**|Die Größe des Identitätsbereichs für den Verleger.|  
|**range**|**bigint**|Die Bereichsgröße der aufeinander folgenden Identitätswerte, die Abonnenten bei einer Anpassung zugewiesen würden.|  
|**max_identity**|**bigint**|Die obere Grenze des Identitätsbereichs.|  
|**threshold**|**int**|Als Prozentsatz angegebener Schwellenwert für den Identitätsbereich.|  
|**current_max**|**bigint**|Der aktuelle maximale Wert, der zugewiesen werden kann, aber nicht notwendigerweise zugewiesen werden muss.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
