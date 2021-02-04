---
description: setMaxFieldSize-Methode (SQLServerStatement)
title: setMaxFieldSize-Methode (SQLServerStatement) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerStatement.setMaxFieldSize
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 38f7fc1d-acad-4d10-9fc8-3c0669d93b07
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: a98cff7f25b30cc5bcb3cb22bd2aab342e790eac
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173363"
---
# <a name="setmaxfieldsize-method-sqlserverstatement"></a>setMaxFieldSize-Methode (SQLServerStatement)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt das Limit für die maximale Anzahl von Bytes in einer [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)-Spalte, in der Zeichen- oder Binärwerte gespeichert werden, auf die angegebene Anzahl von Bytes fest.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public final void setMaxFieldSize(int max)  
```  
  
#### <a name="parameters"></a>Parameter  
 *max*  
  
 Ein Wert vom Typ **int** zum Angeben der maximalen Anzahl der Bytes.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese setMaxFieldSize-Methode wird von der setMaxFieldSize-Methode in der java.sql.Statement-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerStatement-Elemente](../../../connect/jdbc/reference/sqlserverstatement-members.md)   
 [SQLServerStatement-Klasse](../../../connect/jdbc/reference/sqlserverstatement-class.md)  
  
  
