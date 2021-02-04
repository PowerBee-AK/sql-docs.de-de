---
description: getBoolean-Methode (java.lang.String) (SQLServerResultSet)
title: getBoolean-Methode (java.lang.String) (SQLServerResultSet) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.getBoolean (java.lang.String)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: ba98a27b-722d-4904-ac65-0f082fde1fe6
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 28886a0ceea38b0c465de8bde215cbdc277ee829
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99168139"
---
# <a name="getboolean-method-javalangstring-sqlserverresultset"></a>getBoolean-Methode (java.lang.String) (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)-Objekts als **booleschen** Wert in der Programmiersprache Java ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean getBoolean(java.lang.String columnName)  
```  
  
#### <a name="parameters"></a>Parameter  
 *columnName*  
  
 Eine **Zeichenfolge**, die den Spaltennamen enthält.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein **boolescher** Wert.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese getBoolean-Methode wird von der getBoolean-Methode in der java.sql.ResultSet-Schnittstelle angegeben.  
  
 Diese Methode wird nur für Zahlen- und Zeichendatentypen unterstützt. Die Methode konvertiert die Werte „1“, 1 und „**TRUE**“ in **TRUE** und die Werte „0“, 0 und „**FALSE**“ in **FALSE**. Für alle anderen Werte bleibt das Verhalten nicht definiert.  
  
## <a name="see-also"></a>Weitere Informationen  
 [getBoolean Method &#40;SQLServerResultSet&#41;](../../../connect/jdbc/reference/getboolean-method-sqlserverresultset.md)   
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
