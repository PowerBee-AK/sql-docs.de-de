---
description: isClosed-Methode (SQLServerConnection)
title: isClosed-Methode (SQLServerConnection) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerConnection.isClosed
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 3560ab18-4350-4d02-9716-439f0c2f7142
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: c8a524b7d5aa5af4cd002741786ea2fb0cea2bb2
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177460"
---
# <a name="isclosed-method-sqlserverconnection"></a>isClosed-Methode (SQLServerConnection)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt an, ob dieses [SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-class.md)-Objekt geschlossen wurde.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean isClosed()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Der Wert lautet **TRUE**, wenn die Verbindung geschlossen wurde, andernfalls **FALSE**.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese isClosed-Methode wird von der isClosed-Methode in der java.sql.Connection-Schnittstelle angegeben.  
  
 Damit wird der Zustand des aufgerufenen SQLServerConnection-Objekts überprüft. Eine Verbindung wird geschlossen, wenn für sie die [close](../../../connect/jdbc/reference/close-method-sqlserverconnection.md)-Methode aufgerufen wurde oder bestimmte schwerwiegende Fehler aufgetreten sind. Diese Methode gibt nur dann **true** zurück, wenn sie nach dem Aufrufen der close-Methode aufgerufen wurde.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerConnection-Elemente](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection-Klasse](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
