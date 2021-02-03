---
description: MinDbCompatibilityLevel (geometry-Datentyp)
title: MinDbCompatibilityLevel (geometry-Datentyp) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 08/03/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
dev_langs:
- TSQL
helpviewer_keywords:
- MinDbCompatibilityLevel method (geometry)
ms.assetid: c848b974-8ccb-4c5c-a7eb-b019a9538d99
author: MladjoA
ms.author: mlandzic
ms.openlocfilehash: 752d9516dbe58448e857f83fbcf025139d4884b5
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99159391"
---
# <a name="mindbcompatibilitylevel-geometry-data-type"></a>MinDbCompatibilityLevel (geometry-Datentyp)
[!INCLUDE [SQL Server Azure SQL Database ](../../includes/applies-to-version/sql-asdb.md)]

Gibt den minimalen Datenbankkompatibilitätsgrad zurück, der die **geometry** -Datentypinstanz erkennt.
  
## <a name="syntax"></a>Syntax  
  
```  
  
.MinDbCompatibilityLevel ( )  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="return-types"></a>Rückgabetypen
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Rückgabetyp: **int**  
  
 CLR-Rückgabetyp: **int**  
  
## <a name="remarks"></a>Hinweise  
 Testen Sie die Kompatibilität eines räumlichen Objekts mithilfe von `MinDbCompatibilityLevel()` , bevor Sie den Kompatibilitätsgrad einer Datenbank ändern.  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-testing-circularstring-type-for-compatibility-with-compatibility-level-110"></a>A. Testen der Kompatibilität des CircularString-Typs mit Kompatibilitätsgrad 110  
 Im folgenden Beispiel wird die Kompatibilität einer `CircularString`-Instanz mit einer früheren Version von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] getestet:  
  
```
 DECLARE @g geometry = 'CIRCULARSTRING(3 4, 8 9, 5 6)'; 
 IF @g.MinDbCompatibilityLevel() <= 110 
 BEGIN 
 SELECT @g.ToString(); 
 END
 ```  
  
### <a name="b-testing-linestring-type-for-compatibility-with-compatibility-level-100"></a>B. Testen der Kompatibilität des LineString-Typs mit Kompatibilitätsgrad 100  
 Im folgenden Beispiel wird die Kompatibilität einer `LineString` -Instanz mit [!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)]getestet:  
  
```
 DECLARE @g geometry = 'LINESTRING(3 4, 8 9, 5 6)'; 
 IF @g.MinDbCompatibilityLevel() <= 100 
 BEGIN 
 SELECT @g.ToString(); 
 END
``` 
  
## <a name="see-also"></a>Weitere Informationen  
 [ALTER DATABASE-Kompatibilitätsgrad &#40;Transact-SQL&#41;](../../t-sql/statements/alter-database-transact-sql-compatibility-level.md)  
  
  

