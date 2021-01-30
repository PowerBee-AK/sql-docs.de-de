---
description: MSsub_identity_range (Transact-SQL)
title: MSsub_identity_range (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSsub_identity_range_TSQL
- MSsub_identity_range
dev_langs:
- TSQL
helpviewer_keywords:
- MSsub_identity_range system table
ms.assetid: 26e20d28-14ed-44fc-af3b-4de386de4bb8
author: cawrites
ms.author: chadam
ms.openlocfilehash: b57fc0593298e38f6db8969e742127c007411246
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99156795"
---
# <a name="mssub_identity_range-transact-sql"></a>MSsub_identity_range (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MSsub_identity_range** Tabelle bietet Unterstützung für die Identitäts Bereichs Verwaltung für Abonnements. Diese Tabelle wird in Abonnementdatenbanken gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**objid**|**int**|Die ID der Tabelle, die die durch Replikation verwaltete Identitätsspalte enthält.|  
|**range**|**bigint**|Steuert die Bereichsgröße der aufeinander folgenden Identitätswerte, die auf dem Abonnenten bei einer Anpassung zugewiesen würden.|  
|**last_seed**|**bigint**|Die untere Grenze des aktuellen Bereichs.|  
|**threshold**|**int**|Der Prozentwert, der steuert, wann der Verteilungs-Agent einen neuen Identitätsbereich zuweist. Wenn der in *Schwellenwert* angegebene Prozentsatz der Werte verwendet wird, erstellt der Verteilungs-Agent einen neuen Identitäts Bereich.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
