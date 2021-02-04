---
description: getLastUpdateCount-Methode (SQLServerDataSource)
title: getLastUpdateCount-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.getLastUpdateCount
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 4c4fbb24-0b02-42da-928c-a903bb591cc7
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: bf2a9772d3fd6c97b9416e810ec3d5680ad3f559
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99162894"
---
# <a name="getlastupdatecount-method-sqlserverdatasource"></a>getLastUpdateCount-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob die lastUpdateCount-Eigenschaft aktiviert ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean getLastUpdateCount()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 **TRUE**, wenn lastUpdateCount aktiviert ist. Andernfalls lautet der Wert **false**.  
  
## <a name="remarks"></a>Bemerkungen  
 Ist die lastUpdateCount-Eigenschaft auf **true** festgelegt, wird von [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] nur die letzte Updatezählung aus einer an den Server übergebenen SQL-Anweisung zurückgegeben. Ist die lastUpdateCount-Eigenschaft auf **false** festgelegt, werden vom Treiber alle Updatezählungen zurückgegeben, einschließlich jener, die von möglicherweise ausgelösten Triggern zurückgegeben wurden. Ist die lastUpdateCount-Eigenschaft nicht festgelegt, wird von der getLastUpdateCount-Methode der Standardwert **true** zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
