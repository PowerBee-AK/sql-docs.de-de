---
description: getFailoverPartner-Methode (SQLServerDataSource)
title: Methode „getFailoverPartner“ (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.getFailoverPartner
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 885f927f-9c48-42e0-a7fb-fd936d2b8130
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: b5084e93cbe03ef79e5858757bf8b627991d9902
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99163053"
---
# <a name="getfailoverpartner-method-sqlserverdatasource"></a>getFailoverPartner-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt den Namen des Failoverservers zurück, der in einer Datenbankspiegelungskonfiguration verwendet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public string getFailoverPartner()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Eine **Zeichenfolge**, die den Namen des Failoverpartners oder NULL enthält, sofern kein Name festgelegt ist.  
  
## <a name="remarks"></a>Hinweise  
 Der von dieser Methode zurückgegebene Wert gibt den Failoverpartnernamen wieder, der mithilfe der [setFailoverPartner](../../../connect/jdbc/reference/setfailoverpartner-method-sqlserverdatasource.md)-Methode festgelegt wurde.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
