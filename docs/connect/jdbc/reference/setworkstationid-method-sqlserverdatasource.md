---
description: setWorkstationID-Methode (SQLServerDataSource)
title: setWorkstationID-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.setWorkstationID
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: c1093615-90bf-4918-9f05-8abd765ffb03
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 8b0047a866a34f68fe1f4f2be9d51714f04fba73
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99172903"
---
# <a name="setworkstationid-method-sqlserverdatasource"></a>setWorkstationID-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt den Namen des Clientcomputers fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void setWorkstationID(java.lang.String workstationID)  
```  
  
#### <a name="parameters"></a>Parameter  
 *workstationID*  
  
 Eine **Zeichenfolge** mit dem Computernamen des Clients.  
  
## <a name="remarks"></a>Hinweise  
 Die workstationID ist der Name des Clientcomputers oder der Workstation. Ist die workstationID-Eigenschaft nicht festgelegt, wird der Standardwert durch Aufruf der InetAddress.getLocalHost().getHostName()-Methode erstellt. Wenn getHostName einen leeren Wert zurückgibt, wird die Methode „getHostAddress().toString()“ aufgerufen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
