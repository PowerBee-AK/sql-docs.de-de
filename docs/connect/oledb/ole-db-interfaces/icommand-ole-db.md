---
title: ICommand (OLE DB-Treiber) | Microsoft-Dokumentation
description: Lernen Sie das Verhalten der ICommand::Execute-Methode kennen, die spezifisch für den OLE DB-Treiber für SQL Server ist.
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ICommand [OLE DB Driver for SQL Server]
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d7d290800b0f002f2ad7ba1703683648a62f41f8
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99191806"
---
# <a name="icommand-ole-db"></a>ICommand (OLE DB)
[!INCLUDE [SQL Server](../../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  In diesem Artikel wird das OLE DB-Verhalten erläutert, das für den OLE DB-Treiber für SQL Server spezifisch ist.  
  
## <a name="icommandexecute"></a>ICommand::Execute  
 Das Einfügen von Daten, die größer als die Größe einer Spalte sind, führt in der Regel zu einem Fehler. Es gibt jedoch Situationen, in denen S_OK zurückgegeben wird und `dwStatus` auf DBSTATUS_S_TRUNCATED festgelegt ist. Es folgen einige Szenarien, in denen dies normalerweise vorkommt:

- Beim Einfügen von Daten mit Parametern  
- Wenn die Spalte nicht groß genug für die Daten ist  
- Wenn `ICommandWithParameters::SetParameterInfo` nicht aufgerufen wurde  
  
## <a name="see-also"></a>Weitere Informationen  
 [Schnittstellen &#40;OLE DB&#41;](../../oledb/ole-db-interfaces/oledb-driver-for-sql-server-ole-db-interfaces.md)
  
  
