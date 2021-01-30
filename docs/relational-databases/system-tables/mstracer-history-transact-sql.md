---
description: MStracer_history (Transact-SQL)
title: MStracer_history (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MStracer_history
- MStracer_history_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MStracer_history system table
ms.assetid: 97237a0c-d574-4b17-8a94-1a8730b31d98
author: cawrites
ms.author: chadam
ms.openlocfilehash: c419865662e3a88bf327035376ddc8a383dbd591
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99211566"
---
# <a name="mstracer_history-transact-sql"></a>MStracer_history (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  In der **MStracer_history** Tabelle wird ein Datensatz aller Überwachungs Token verwaltet, die auf dem Abonnenten empfangen wurden. Diese Tabelle wird in der Verteilungsdatenbank gespeichert. Sie wird von der Replikation für die Leistungsüberwachung verwendet.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**parent_tracer_id**|**int**|Die eindeutige Identifikation eines Überwachungstokens.|  
|**agent_id**|**int**|Identifiziert den Agent, der den Überwachungstokendatensatz behandelt hat.|  
|**subscriber_commit**|**datetime**|Das Datum und die Uhrzeit, zu denen der Commit des Überwachungstokendatensatzes auf dem Abonnenten durchgeführt wurde.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
