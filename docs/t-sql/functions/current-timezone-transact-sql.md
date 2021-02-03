---
description: CURRENT_TIMEZONE (Transact-SQL)
title: CURRENT_TIMEZONE (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 05/28/2020
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- CURRENT_TIMEZONE
- CURRENT_TIMEZONE_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- current time zone [SQL Server]
- current timezone [SQL Server]
- system time zone [SQL Server]
- system timezone [SQL Server]
- functions [SQL Server], time zone
- functions [SQL Server], timezone
- timezone [SQL Server], functions
- time zone [SQL Server], functions
- CURRENT_TIMEZONE function [SQL Server]
author: MladjoA
ms.author: mlandzic
ms.openlocfilehash: 84b9c6c51831c911fdd90741839a49a621225bae
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99184043"
---
# <a name="current_timezone-transact-sql"></a>CURRENT_TIMEZONE (Transact-SQL)

[!INCLUDE[Azure SQL Database Azure SQL Managed Instance](../../includes/applies-to-version/asdb-asdbmi.md)]

Diese Funktion gibt den Namen der von einem Server oder einer Instanz verwendeten Zeitzone zurück. Bei SQL Managed Instance basiert der Rückgabewert auf der Zeitzone der Instanz selbst, die während der Erstellung der Instanz zugewiesen wurde, und nicht auf der Zeitzone des zugrunde liegenden Betriebssystems.
  
> [!NOTE]  
> Bei SQL-Datenbank wird die Zeitzone immer auf UTC festgelegt, und `CURRENT_TIMEZONE` gibt den Namen der UTC-Zeitzone zurück.
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
CURRENT_TIMEZONE ( )  
```
  
## <a name="arguments"></a>Argumente

Diese Funktion akzeptiert keine Argumente.
  
## <a name="return-type"></a>Rückgabetyp  

**varchar**
  
## <a name="remarks"></a>Bemerkungen  

`CURRENT_TIMEZONE` ist eine nicht deterministische Funktion. Sichten und Ausdrücke, die auf diese Spalte verweisen, können nicht indiziert werden.
  
## <a name="example"></a>Beispiel

Beachten Sie, dass der zurückgegebene Wert die tatsächliche Zeitzone und die Spracheinstellungen des Servers oder der Instanz widerspiegelt.

```sql
SELECT CURRENT_TIMEZONE();  
/* Returned:  
(UTC+01:00) Amsterdam, Berlin, Bern, Rome, Stockholm, Vienna 
*/
```  
  
## <a name="see-also"></a>Weitere Informationen

[SQL Managed Instance: Zeitzone](/azure/sql-database/sql-database-managed-instance-timezone)

[CURRENT_TIMEZONE_ID()](./current-timezone-id-transact-sql.md)