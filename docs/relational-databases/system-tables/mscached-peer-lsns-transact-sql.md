---
description: MScached_peer_lsns (Transact-SQL)
title: MScached_peer_lsns (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MScached_peer_lsns_TSQL
- MScached_peer_lsns
dev_langs:
- TSQL
helpviewer_keywords:
- MScached_peer_lsns system table
ms.assetid: f8b6089a-0230-45f9-8c34-9fe0d2a3a74e
author: cawrites
ms.author: chadam
ms.openlocfilehash: 974f15aa4e1c971f6f3ca6abe6d9a31129611dfd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99160492"
---
# <a name="mscached_peer_lsns-transact-sql"></a>MScached_peer_lsns (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MScached_peer_lsns** Tabelle dient zum Nachverfolgen der LSN-Werte im Transaktionsprotokoll, mit denen bestimmt wird, welche Befehle bei der Peer-zu-Peer-Replikation an einen bestimmten Abonnenten zurückgegeben werden. Diese Tabelle wird in der Verteilungsdatenbank gespeichert.  
  
## <a name="definition"></a>Definition  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**agent_id**|**int**|Die ID des Verteilungs-Agents.|  
|**originator**|**sysname**|Der Name des ursprünglichen Verlegers.|  
|**originator_db**|**sysname**|Der Name der ursprünglichen Veröffentlichungsdatenbank.|  
|**originator_publication_id**|**int**|Kennzeichnet die ursprüngliche Veröffentlichung.|  
|**originator_db_version**|**int**|Kennzeichnet die Versionsnummer der ursprünglichen Datenbank.|  
|**originator_lsn**|**varbinary(16)**|Die LSN der ursprünglichen Transaktion.|  
  
## <a name="remarks"></a>Bemerkungen  
 LSN-Werte werden nur unmittelbar nach der Einfügung verwendet. Sie haben keine andauernde Bedeutung im System.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
