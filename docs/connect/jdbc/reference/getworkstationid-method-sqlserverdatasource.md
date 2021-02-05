---
description: getWorkstationID-Methode (SQLServerDataSource)
title: getWorkstationID-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.getWorkstationID
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: f6a701de-a8fa-4668-9310-99a8c6e32c88
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: a4312e32f1b6a9884600b7f521634605612577a2
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177601"
---
# <a name="getworkstationid-method-sqlserverdatasource"></a>getWorkstationID-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt den Namen des Clientcomputers zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.lang.String getWorkstationID()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Eine **Zeichenfolge** mit dem Computernamen des Clients.  
  
## <a name="remarks"></a>Hinweise  
 Die workstationID ist der Name des Clientcomputers oder der Workstation. Ist die workstationID-Eigenschaft nicht festgelegt, wird der Standardwert durch Aufruf der InetAddress.getLocalHost().getHostName()-Methode erstellt. Wenn getHostName einen leeren Wert zurückgibt, wird die Methode „getHostAddress().toString()“ aufgerufen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
