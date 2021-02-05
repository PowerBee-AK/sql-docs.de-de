---
description: moveToCurrentRow-Methode (SQLServerResultSet)
title: moveToCurrentRow-Methode (SQLServerResultSet) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.moveToCurrentRow
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 9a7c754c-2d72-4207-b3bd-2afc6047fb3d
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 8f7e8259fda0a9ec0e17c7cd97f7d5754fbfbcfb
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177023"
---
# <a name="movetocurrentrow-method-sqlserverresultset"></a>moveToCurrentRow-Methode (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Versetzt den Cursor an die gespeicherte Cursorposition (üblicherweise die aktuelle Zeile).  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void moveToCurrentRow()  
```  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese moveToCurrentRow-Methode wird von der moveToCurrentRow-Methode in der java.sql.ResultSet-Schnittstelle angegeben.  
  
 Die Methode zeigt keine Auswirkungen, wenn der Cursor sich nicht in der Einfügezeile befindet.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
