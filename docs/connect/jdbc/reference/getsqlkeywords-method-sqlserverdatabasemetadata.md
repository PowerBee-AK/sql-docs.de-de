---
description: getSQLKeywords-Methode (SQLServerDatabaseMetaData)
title: getSQLKeywords-Methode (SQLServerDatabaseMetaData) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDatabaseMetaData.getSQLKeywords
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: a2a0dfbb-11ec-429f-aea6-8f44148ebb8e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 8e2f7578ffea15444d218bde08eef68634632b41
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99175018"
---
# <a name="getsqlkeywords-method-sqlserverdatabasemetadata"></a>getSQLKeywords-Methode (SQLServerDatabaseMetaData)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft eine durch Trennzeichen getrennte Liste mit allen SQL-Schlüsselwörtern dieser Datenbank ab, bei denen es sich nicht gleichzeitig um SQL92-Schlüsselwörter handelt.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.lang.String getSQLKeywords()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Eine **Zeichenfolge** mit den SQL-Schlüsselwörtern.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese getSQLKeywords-Methode wird von der getSQLKeywords-Methode in der java.sql.DatabaseMetaData-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDatabaseMetaData-Methoden](../../../connect/jdbc/reference/sqlserverdatabasemetadata-methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../../../connect/jdbc/reference/sqlserverdatabasemetadata-members.md)   
 [SQLServerDatabaseMetaData-Klasse](../../../connect/jdbc/reference/sqlserverdatabasemetadata-class.md)  
  
  
