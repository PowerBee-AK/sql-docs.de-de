---
description: rollback-Methode ()
title: rollback()-Methode | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerConnection.rollback ()
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 7adb6772-4047-4d8e-931d-b3d20eec44b5
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: cc5f37ecd5965600a68a3df7dbdb3484fd6b6658
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99174083"
---
# <a name="rollback-method-"></a>rollback-Methode ()
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Macht alle im Rahmen der aktuellen Transaktion vorgenommenen Änderungen rückgängig und hebt sämtliche Datenbanksperren auf, die derzeit von diesem [SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-class.md)-Objekt aufrecht erhalten werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void rollback()  
```  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese rollBack-Methode wird von der rollBack-Methode in der java.sql.Connection-Schnittstelle angegeben.  
  
 Die Methode sollte nur bei deaktiviertem Modus für automatische Commits verwendet werden.  
  
## <a name="see-also"></a>Weitere Informationen  
 [rollback-Methode &#40;SQLServerConnection&#41;](../../../connect/jdbc/reference/rollback-method-sqlserverconnection.md)   
 [SQLServerConnection-Elemente](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection-Klasse](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
