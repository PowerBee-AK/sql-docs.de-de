---
description: setFetchDirection-Methode (SQLServerResultSet)
title: setFetchDirection-Methode (SQLServerResultSet) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.setFetchDirection
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 4ee82290-508d-4bff-a5c5-8a56338deef8
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: b6b7a2ab02e084a0dabdba76cb1f32182d84f1de
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173480"
---
# <a name="setfetchdirection-method-sqlserverresultset"></a>setFetchDirection-Methode (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt Aufschluss über die Richtung, in der die Zeilen in diesem [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)-Objekt verarbeitet werden.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] derzeit nicht unterstützt. Bei Verwendung dieser Methode wird die Einstellung vom JDBC-Treiber zwar gespeichert, sie wird jedoch derzeit nicht genutzt.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void setFetchDirection(int direction)  
```  
  
#### <a name="parameters"></a>Parameter  
 *direction*  
  
 Ein Wert vom Typ **int** zum Angeben der vorgeschlagenen Abrufrichtung. Folgenden Werte sind möglich:  
  
 ResultSet.FETCH_FORWARD  
  
 ResultSet.FETCH_REVERSE  
  
 ResultSet.FETCH_UNKNOWN  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese setFetchDirection-Methode wird von der setFetchDirection-Methode in der java.sql.ResultSet-Schnittstelle angegeben.  
  
 Der Anfangswert dieser Methode wird vom [SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md)-Objekt bestimmt, von dem dieses SQLServerResultSet-Objekt erstellt wurde. Die Abrufrichtung kann jedoch jederzeit geändert werden.  
  
> [!NOTE]  
>  Handelt es sich beim Cursortyp um einen Vorwärtscursor, hat die Verwendung dieser Methode keine Auswirkungen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
