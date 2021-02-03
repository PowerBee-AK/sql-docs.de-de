---
description: AsBinaryZM (geometry-Datentyp)
title: AsBinaryZM (geometry-Datentyp) | Microsoft-Dokumentation
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
- AsBinaryZM geometry
ms.assetid: 5eae2872-adca-4b8f-8b04-4ee91ced98f1
author: MladjoA
ms.author: mlandzic
ms.openlocfilehash: 2eed08ad181f5a16277facd5b892d4787073bffc
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187731"
---
# <a name="asbinaryzm-geometry-datatype"></a>AsBinaryZM (geometry-Datentyp)
[!INCLUDE [SQL Server Azure SQL Database ](../../includes/applies-to-version/sql-asdb.md)]

Gibt die Open Geospatial Consortium (OGC) WKB-Darstellung (Well-Known Binary) einer **geometry**-Instanz zurück, die um alle von der Instanz getragenen **Z**- (Höhe) und **M**-Werte (Measure) erweitert wurde.
  
## <a name="syntax"></a>Syntax  
  
```  
  
.AsBinaryZM()  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="return-types"></a>Rückgabetypen
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Rückgabetyp: **varbinary(max)**  
  
 CLR-Rückgabetyp: **SqlBytes**  
  
## <a name="remarks"></a>Bemerkungen  
  
## <a name="examples"></a>Beispiele  
  
```sql  
DECLARE @g1 GEOMETRY = 'Point(1 1 2 3)';  
  
SELECT @g1.STAsBinary();  
-- Returns: 0x0101000000000000000000F03F000000000000F03F  
  
SELECT @g1.AsBinaryZM();  
--Returns: 0x01B90B0000000000000000F03F000000000000F03F00000000000000400000000000000840  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Erweiterte Methoden für geometry-Instanzen](../../t-sql/spatial-geometry/extended-methods-on-geometry-instances.md)   
 [M &#40;geometry-Datentyp&#41;](../../t-sql/spatial-geometry/m-geometry-data-type.md)   
 [Z &#40;geometry Data Type&#41; (Z (geometry-Datentyp))](../../t-sql/spatial-geometry/z-geometry-data-type.md)  
  
  

