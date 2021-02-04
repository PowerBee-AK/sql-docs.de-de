---
description: absolute-Methode (SQLServerResultSet)
title: absolute-Methode (SQLServerResultSet) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.absolute
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 638e8148-8ca0-4e1f-9ec2-04a11bc9809b
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 1eae674d751cf688a8fc3ae4feb04a3867b3ee04
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99163601"
---
# <a name="absolute-method-sqlserverresultset"></a>absolute-Methode (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Versetzt den Cursor in die vorhandene Zeile in diesem [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)-Objekt.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean absolute(int row)  
```  
  
#### <a name="parameters"></a>Parameter  
 *row*  
  
 Ein Wert vom Typ **int** zum Angeben der Zeilenzahl, an die verschoben werden soll. Kann positiv, negativ oder "0" sein.  
  
## <a name="return-value"></a>Rückgabewert  
 **TRUE**, wenn der Cursor an die gegebene Position bewegt wird. **FALSE**, wenn sich der Cursor vor der ersten oder nach der letzten Zeile befindet.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese absolute-Methode wird von der absolute-Methode in der java.sql.ResultSet-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
