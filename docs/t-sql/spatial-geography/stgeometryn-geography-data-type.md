---
description: STGeometryN (geography-Datentyp)
title: STGeometryN (geography-Datentyp) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- STGeometryN (geography Data Type)
dev_langs:
- TSQL
helpviewer_keywords:
- STGeometryN method
ms.assetid: 53755f69-cd50-475b-b3b8-a1a9157cf03a
author: MladjoA
ms.author: mlandzic
ms.openlocfilehash: 875baefa0f1795bc1913a42e98705668364dae04
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199029"
---
# <a name="stgeometryn-geography-data-type"></a>STGeometryN (geography-Datentyp)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

  Gibt ein bestimmtes **geography**-Element in einer **GeometryCollection** oder in einem ihrer Untertypen zurück. Wenn STGeometryN() für den Untertyp einer **GeometryCollection** wie **MultiPoint** oder **MultiLineString** verwendet wird, gibt diese Methode bei einem Aufruf mit N=1 die **geography**-Instanz zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
.STGeometryN ( expression )  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="arguments"></a>Argumente
 *expression*  
 Ein **int**-Ausdruck zwischen 1 und der Anzahl der **geography**-Instanzen in der **GeometryCollection**.  
  
## <a name="return-types"></a>Rückgabetypen  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Rückgabetyp: **geography**  
  
 CLR-Rückgabetyp: **SqlGeography**  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Methode gibt NULL zurück, wenn der Parameter größer als das Ergebnis von [STNumGeometries()](../../t-sql/spatial-geography/stnumgeometries-geography-data-type.md) ist und löst eine **ArgumentOutOfRangeException** aus, wenn der *expression*-Parameter kleiner als 1 ist.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel wird eine `MultiPoint``geography`-Instanz erstellt und `STGeometryN()` verwendet, um nach der zweiten `geography`-Instanz in der **GeometryCollection** zu suchen.  
  
```  
DECLARE @g geography;  
SET @g = geography::STGeomFromText('MULTIPOINT(-122.360 47.656, -122.343 47.656)', 4326);  
SELECT @g.STGeometryN(2).ToString();  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [OGC-Methoden für geography-Instanzen](../../t-sql/spatial-geography/ogc-methods-on-geography-instances.md)  
  
  
