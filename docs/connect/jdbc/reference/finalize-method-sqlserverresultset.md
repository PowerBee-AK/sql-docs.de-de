---
description: finalize-Methode (SQLServerResultSet)
title: finalize-Methode (SQLServerResultSet) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.finalize
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 49bc879d-822b-42da-bc20-2394865f1f0f
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 71dc58e3172657a480aa5465e48010953c32fc83
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99168433"
---
# <a name="finalize-method-sqlserverresultset"></a>finalize-Methode (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Schließt dieses [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)-Objekt explizit.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void finalize()  
```  
  
## <a name="remarks"></a>Hinweise  
 Schließt das Resultset, wenn dies nicht durch die Anwendung geschieht. Diese Methode entspricht der JDBC-Spezifikation. Da die Java Virtual Machine (JVM) keine Garantie dafür bietet, wann ein Finalizer ausgeführt werden kann, können Anwendungen, von denen ihre Resultsets nicht explizit geschlossen werden, einen Deadlock für eine andere Anweisung auslösen, von der die gleiche Verbindung verwendet wird und die für eine gemeinsame Serverressource (z. B. Zeilensperren) blockiert wird.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
