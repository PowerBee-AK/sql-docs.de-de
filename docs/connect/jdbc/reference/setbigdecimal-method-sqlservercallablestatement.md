---
description: setBigDecimal-Methode (SQLServerCallableStatement)
title: Methode „setBigDecimal“ (SQLServerCallableStatement) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerCallableStatement.setBigDecimal
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: b50a920c-3839-40f0-9411-c60bbc2a9f34
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 600a9d354f3c14dc4b2240639ff4a136df2949be
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173936"
---
# <a name="setbigdecimal-method-sqlservercallablestatement"></a>setBigDecimal-Methode (SQLServerCallableStatement)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt die angegebene Parameternummer auf das angegebene BigDecimal-Objekt fest.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void setBigDecimal(java.lang.String sCol,  
                          java.math.BigDecimal bd)  
```  
  
#### <a name="parameters"></a>Parameter  
 *sCol*  
  
 Ein **String-Objekt**, das den Parameternamen enthält.  
  
 *bd*  
  
 Ein BigDecimal-Objekt  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese setBigDecimal-Methode wird von der setBigDecimal-Methode in der java.sql.CallableStatement-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerCallableStatement-Elemente](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)   
 [SQLServerCallableStatement-Klasse](../../../connect/jdbc/reference/sqlservercallablestatement-class.md)  
  
  
