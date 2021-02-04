---
description: addConnectionEventListener-Methode (SQLServerPooledConnection)
title: addConnectionEventListener-Methode (SQLServerPooledConnection) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerPooledConnection.addConnectionEventListener
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 142830a8-8d4e-48ca-911d-85bf195ca4fe
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 2354562eb4cdfc81145aaf139e2cd5cdc776d2cd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99163567"
---
# <a name="addconnectioneventlistener-method-sqlserverpooledconnection"></a>addConnectionEventListener-Methode (SQLServerPooledConnection)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Registriert den angegebenen Ereignislistener, damit dieser benachrichtigt wird, wenn in Zusammenhang mit dem [SQLServerPooledConnection](../../../connect/jdbc/reference/sqlserverpooledconnection-class.md)-Objekt ein Ereignis auftritt.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void addConnectionEventListener(javax.sql.ConnectionEventListener listener)  
```  
  
#### <a name="parameters"></a>Parameter  
 *listener*  
  
 Dies ist ein ConnectionEventListener-Objekt.  
  
## <a name="remarks"></a>Bemerkungen  
 Diese addConnectionEventListener-Methode wird von der addConnectionEventListener-Methode in der javax.sql.PooledConnection-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerPooledConnection-Methoden](../../../connect/jdbc/reference/sqlserverpooledconnection-methods.md)   
 [SQLServerPooledConnection-Elemente](../../../connect/jdbc/reference/sqlserverpooledconnection-members.md)   
 [SQLServerPooledConnection-Klasse](../../../connect/jdbc/reference/sqlserverpooledconnection-class.md)  
  
  
