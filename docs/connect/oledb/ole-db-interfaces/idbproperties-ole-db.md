---
title: IDBProperties (OLE DB-Treiber) | Microsoft-Dokumentation
description: Erfahren Sie mehr über die IDBProperties-Schnittstelle im OLE DB-Treiber für SQL Server, einschließlich IDBProperties::GetPropertyInfo-Methode.
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 57f0d5da55d3a3a4c424f8467dac0f55ca410de3
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99186822"
---
# <a name="idbproperties-ole-db"></a>IDBProperties (OLE DB)
[!INCLUDE [SQL Server](../../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  Dank der OLE DB-Standardspezifikation können Anbieter VT_EMPTY für **DBPROPINFO::vValues** angeben. Vom OLE DB-Treiber für SQL Server wird jedoch immer VT_EMPTY zurückgegeben, wenn Sie **IDBProperties::GetPropertyInfo** zum Abrufen von Rowseteigenschaften zusammen mit **DBPROPSET_ROWSETALL** aufrufen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Schnittstellen &#40;OLE DB&#41;](../../oledb/ole-db-interfaces/oledb-driver-for-sql-server-ole-db-interfaces.md) 
  
  
