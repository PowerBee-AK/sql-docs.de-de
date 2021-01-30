---
description: MSreplication_options (Transact-SQL)
title: MSreplication_options (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- MSreplication_options
- MSreplication_options_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSreplication_options system table
ms.assetid: 23cf10d7-8bc1-4368-b5eb-e5576421e776
author: cawrites
ms.author: chadam
ms.openlocfilehash: e5df7d73eab0c5766468b59207b29ecb45e2e56e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199069"
---
# <a name="msreplication_options-transact-sql"></a>MSreplication_options (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  In der **MSreplication_options** Tabelle werden Metadaten gespeichert, die intern von der Replikation verwendet werden. Diese Tabelle wird in der **Master** -Datenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**optname**|**sysname**|Nur zur internen Verwendung.|  
|**value**|**bit**|Nur zur internen Verwendung.|  
|**major_version**|**int**|Nur zur internen Verwendung.|  
|**minor_version**|**int**|Nur zur internen Verwendung.|  
|**revision**|**int**|Nur zur internen Verwendung.|  
|**install_failures**|**int**|Nur zur internen Verwendung.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikationstabellen &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)  
  
  
