---
description: sqlsrv_has_rows
title: sqlsrv_has_rows | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- API Reference, sqlsrv_has_rows
- sqlsrv_has_rows
ms.assetid: 4da7f640-cf12-409f-9e00-95b30a8d5e17
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: eaef86b083291f8ae73ab5d9a89060f634d30491
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99153929"
---
# <a name="sqlsrv_has_rows"></a>sqlsrv_has_rows
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

Zeigt an, ob das Resultset eine oder mehrere Zeilen enthält.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sqlsrv_has_rows( resource $stmt )  
```  
  
#### <a name="parameters"></a>Parameter  
*$stmt*: ausgeführte Anweisung.  
  
## <a name="return-value"></a>Rückgabewert  
Falls das Resultset Zeilen enthält, wird der zurückgegebene Wert **true** sein. Falls es keine Zeilen gibt oder der Funktionsaufruf fehlschlägt, ist der zurückgegebene Wert **false**.  
  
## <a name="example"></a>Beispiel  
  
```  
<?php  
   $server = "server_name";  
   $conn = sqlsrv_connect( $server, array( 'Database' => 'Northwind' ) );  
  
   $stmt = sqlsrv_query( $conn, "select * from orders where CustomerID = 'VINET'" , array());  
  
   if ($stmt !== NULL) {  
      $rows = sqlsrv_has_rows( $stmt );  
  
      if ($rows === true)  
         echo "\nthere are rows\n";  
      else   
         echo "\nno rows\n";  
   }  
?>  
```  
  
## <a name="see-also"></a>Weitere Informationen  
[API-Referenz für den SQLSRV-Treiber](../../connect/php/sqlsrv-driver-api-reference.md)  
  
