---
description: setCatalog-Methode (SQLServerConnection)
title: setCatalog-Methode (SQLServerConnection) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerConnection.setCatalog
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 553c0603-c07d-436a-86eb-3ba6b51bd696
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d7c72a4f3198f1d38906288a5c5cec8f3873cb53
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173739"
---
# <a name="setcatalog-method-sqlserverconnection"></a>setCatalog-Methode (SQLServerConnection)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt den angegebenen Katalognamen fest, um einen Teilbereich der Datenbank dieses [SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-class.md)-Objekts auszuwählen, in dem gearbeitet werden soll.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void setCatalog(java.lang.String catalog)  
```  
  
#### <a name="parameters"></a>Parameter  
 *catalog*  
  
 Ein **String-Objekt**, das den Katalognamen enthält.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese setCatalog-Methode wird von der setCatalog-Methode in der java.sql.Connection-Schnittstelle angegeben.  
  
 Das *catalog*-Argument wird automatisch von [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] mit Escapezeichen versehen. Bei Verwendung dieser Methode wird die catalog-Eigenschaft für das Connection-Objekt festgelegt. Diese wird auf keine andere Weise implizit festgelegt.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerConnection-Elemente](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection-Klasse](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
