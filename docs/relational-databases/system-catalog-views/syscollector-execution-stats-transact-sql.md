---
description: syscollector_execution_stats (Transact-SQL)
title: syscollector_execution_stats (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- syscollector_execution_stats
- syscollector_execution_stats_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- syscollector_execution_stats view
- data collector view
ms.assetid: 23e35ac5-fbbf-4922-970c-f4fac44c1263
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: 54a56a6a9bdb2e5ad783d2e860c0b3415d4ddf7c
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199713"
---
# <a name="syscollector_execution_stats-transact-sql"></a>syscollector_execution_stats (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Stellt Informationen zur Taskausführung für einen Sammlungssatz oder ein Paket bereit.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**log_id**|**bigint**|Identifiziert jede Sammlungssatzausführung. Wird verwendet, um diese Sicht mit anderen ausführlichen Protokollen zu verknüpfen. Lässt keine NULL-Werte zu.|  
|**task_name**|**nvarchar(128)**|Der Name des Sammlungssatz- oder Pakettasks, auf den sich diese Informationen beziehen. Lässt keine NULL-Werte zu.|  
|**execution_row_count_in**|**int**|Anzahl der Zeilen, die zu Beginn des Datenflusses verarbeitet wurden. Lässt NULL-Werte zu.|  
|**execution_row_count_out**|**int**|Anzahl der Zeilen, die am Ende des Datenflusses verarbeitet wurden. Lässt NULL-Werte zu.|  
|**execution_row_count_errors**|**int**|Anzahl der Zeilen, bei denen während des Datenflusses ein Fehler aufgetreten ist. Lässt NULL-Werte zu.|  
|**execution_time_ms**|**int**|Die für den Abschluss des Tasks erforderliche Zeit in Millisekunden. Lässt NULL-Werte zu.|  
|**log_time**|**datetime**|Der Zeitpunkt, zu dem diese Informationen protokolliert wurden. Lässt keine NULL-Werte zu.|  
  
## <a name="permissions"></a>Berechtigungen  
 Erfordert die SELECT-Berechtigung für **dc_operator**.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Gespeicherte Prozeduren für den Datensammler &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/data-collector-stored-procedures-transact-sql.md)   
 [Sichten des Datensammlers &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/data-collector-views-transact-sql.md)   
 [Datensammlung](../../relational-databases/data-collection/data-collection.md)  
  
  
