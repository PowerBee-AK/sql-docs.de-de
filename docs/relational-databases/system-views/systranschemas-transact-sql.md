---
description: systranschemas (Transact-SQL)
title: systranschemas (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- systranschemas
- systranschemas_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- systranschemas system table
ms.assetid: 864c3966-cb61-4f2b-8939-ccda112de853
author: stevestein
ms.author: sstein
ms.openlocfilehash: 78242bbe5df333aa23dfd2b8c22688ef5e2e6284
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99181540"
---
# <a name="systranschemas-transact-sql"></a>systranschemas (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **systranschemas** -Tabelle dient zum Nachverfolgen von Schema Änderungen in Artikeln, die in Transaktions-und Momentaufnahme Veröffentlichungen veröffentlicht werden. Diese Tabelle wird sowohl in Veröffentlichungs- als auch in Abonnementdatenbanken gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**tabid**|**int**|Identifiziert den Tabellenartikel, in dem die Schemaänderung stattgefunden hat.|  
|**startlsn**|**binary**|LSN-Wert zu Beginn der Schemaänderung|  
|**endlsn**|**binary**|LSN-Wert am Ende der Schemaänderung|  
|**TypeId**|**int**|Art der Schemaänderung|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikationstabellen &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)  
  
  
