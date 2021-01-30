---
title: sys.remote_data_archive_databases (Transact-SQL) | Microsoft-Dokumentation
description: Erfahren Sie, wie sys.remote_data_archive_databases eine Zeile für jede Remote Datenbank enthält, in der Daten aus einer Stretch-aktivierten lokalen Datenbank gespeichert werden.
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.technology: stored-procedures
ms.topic: reference
f1_keywords:
- sys.remote_data_archive_databases
- sys.remote_data_archive_databases_TSQL
- remote_data_archive_databases
- remote_data_archive_databases_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.remote_data_archive_databases catalog view
ms.assetid: 25bffb0c-9821-40b4-88cf-75f854891a09
author: pmasl
ms.author: pelopes
ms.reviewer: mikeray
ms.openlocfilehash: 8ab3672838849626ea5f72f392ae102d8565b749
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99185010"
---
# <a name="stretch-database-catalog-views---sysremote_data_archive_databases"></a>Stretch Database Katalog Sichten-sys.remote_data_archive_databases
[!INCLUDE [sqlserver2016](../../includes/applies-to-version/sqlserver2016.md)]

  Enthält eine Zeile für jede Remote Datenbank, in der Daten aus einer Stretch-aktivierten lokalen Datenbank gespeichert werden.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**remote_database_id**|**int**|Der automatisch generierte lokale Bezeichner der Remote Datenbank.|  
|**remote_database_name**|**sysname**|Der Name der Remote Datenbank.|  
|**data_source_id**|**int**|Die Datenquelle, mit der eine Verbindung mit dem Remote Server hergestellt wird.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Stretch Database](../../sql-server/stretch-database/stretch-database.md)  
  
  
