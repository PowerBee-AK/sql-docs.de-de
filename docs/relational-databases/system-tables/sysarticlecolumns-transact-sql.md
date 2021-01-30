---
description: sysarticlecolumns (Transact-SQL)
title: sysarticlecolumns (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- sysarticlecolumns
- sysarticlecolumns_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sysarticlecolumns system table
ms.assetid: 55918592-e05d-43b6-843b-7e4d82fa6275
author: cawrites
ms.author: chadam
ms.openlocfilehash: a7acd26639a87c509b97643d4876b43eaab13f06
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99191113"
---
# <a name="sysarticlecolumns-transact-sql"></a>sysarticlecolumns (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **sysarticlecolumns** -Tabelle enthält eine Zeile für jede Tabellenspalte, die in einer Momentaufnahme-oder Transaktions Veröffentlichung veröffentlicht wird, und ordnet jede Spalte dem Artikel zu. Diese Tabelle wird in der Veröffentlichungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**artid**|**int**|Identifiziert einen Artikel.|  
|**ColId**|**smallint**|Identifiziert eine Spalte in einem Artikel.|  
|**is_udt**|**bit**|Zeigt an, ob die Spalte dem benutzerdefinierten Datentyp (UDT) zugehört. Der Wert **1** gibt eine UDT-Spalte an.|  
|**is_xml**|**bit**|Gibt an, ob die Spalte eine **XML** -Spalte ist. Der Wert **1** gibt eine XML-Spalte an.|  
|**is_max**|**bit**|Gibt an, ob die Spalte eine Spalte mit einem großen Wert ( **varchar (max)**, **nvarchar (max)** und **varbinary (max)** ist. Der Wert **1** gibt eine Spalte mit großen Werten an.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
