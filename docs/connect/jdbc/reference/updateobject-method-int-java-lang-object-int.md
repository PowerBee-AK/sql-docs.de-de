---
description: updateObject-Methode (int, java.lang.Object, int)
title: updateObject-Methode (int, java.lang.Object, int) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.updateObject (int, java.lang.Object, int)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 9d33571b-4887-49d3-96df-8abda7b5a904
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 55d947254c37cbc123b97ab11994c53540e595c7
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99182926"
---
# <a name="updateobject-method-int-javalangobject-int"></a>updateObject-Methode (int, java.lang.Object, int)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Aktualisiert die angegebene Spalte mit einem Wert vom Typ **Object** unter Verwendung des angegebenen Spaltenindexes und der Dezimalstellen.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void updateObject(int index,  
                         java.lang.Object x,  
                         int scale)  
```  
  
#### <a name="parameters"></a>Parameter  
 *Index*  
  
 Ein **ganzzahliger** Wert, der den Spaltenindex angibt.  
  
 *obj*  
  
 Ein **Object**-Wert.  
  
 *scale*  
  
 Gilt für java.sql.Types.DECIMAL- oder java.sql.Types.NUMERIC-Typen. Dieser Wert gibt die Anzahl der Dezimalstellen an. Bei allen anderen Typen wird dieser Wert ignoriert.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [updateObject-Methode &#40;SQLServerResultSet&#41;](../../../connect/jdbc/reference/updateobject-method-sqlserverresultset.md)   
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
