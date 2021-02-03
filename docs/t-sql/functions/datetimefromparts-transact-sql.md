---
description: DATETIMEFROMPARTS (Transact-SQL)
title: DATETIMEFROMPARTS (Transact-SQL)
ms.custom: ''
ms.date: 01/29/2021
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- DATETIMEFROMPARTS_TSQL
- DATETIMEFROMPARTS
dev_langs:
- TSQL
helpviewer_keywords:
- DATETIMEFROMPARTS function
author: cawrites
ms.author: chadam
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 8cc7cb964f1cd8b56cbb06aa5bccc97aef76a7b4
ms.sourcegitcommit: b1cec968b919cfd6f4a438024bfdad00cf8e7080
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2021
ms.locfileid: "99237904"
---
# <a name="datetimefromparts-transact-sql"></a>DATETIMEFROMPARTS (Transact-SQL)
[!INCLUDE [sql-asdb-asdbmi-asa-pdw](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

Diese Funktion gibt einen **datetime**-Wert für die angegebenen Argumente für Datum und Zeit zurück.
  
![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
DATETIMEFROMPARTS ( year, month, day, hour, minute, seconds, milliseconds )  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="arguments"></a>Argumente
*year*  
Ein ganzzahliger Ausdruck, der ein Jahr angibt.
  
*month*  
Ein ganzzahliger Ausdruck, der einen Monat angibt.
  
*day*  
Ein ganzzahliger Ausdruck, der einen Tag angibt.
  
*hour*  
Ein ganzzahliger Ausdruck, der Stunden angibt.
  
*minute*  
Ein ganzzahliger Ausdruck, der Minuten angibt.
  
*Sekunden*  
Ein ganzzahliger Ausdruck, der Sekunden angibt.
  
*milliseconds*  
Ein ganzzahliger Ausdruck, der Millisekunden angibt.
  
## <a name="return-types"></a>Rückgabetypen
**datetime**
  
## <a name="remarks"></a>Bemerkungen  
`DATETIMEFROMPARTS` gibt einen vollständig initialisierten **datetime**-Wert zurück. `DATETIMEFROMPARTS` löst einen Fehler aus, wenn mindestens ein erforderliches Argument über einen ungültigen Wert verfügt. `DATETIMEFROMPARTS` gibt NULL zurück, wenn mindestens ein erforderliches Argument den Wert NULL enthält.
  
Diese Funktion kann remote auf [!INCLUDE[sssql11-md](../../includes/sssql11-md.md)]-Servern oder höher ausgeführt werden. Eine Remoteausführung auf Servern mit einer Version vor [!INCLUDE[sssql11-md](../../includes/sssql11-md.md)] ist nicht möglich.  
  
## <a name="examples"></a>Beispiele  
  
```sql
SELECT DATETIMEFROMPARTS ( 2010, 12, 31, 23, 59, 59, 0 ) AS Result;  
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
```
Result  
---------------------------  
2010-12-31 23:59:59.000  
  
(1 row(s) affected)  
```  
  
## <a name="see-also"></a>Weitere Informationen
[datetime &#40;Transact-SQL&#41;](../../t-sql/data-types/datetime-transact-sql.md)
  
  

