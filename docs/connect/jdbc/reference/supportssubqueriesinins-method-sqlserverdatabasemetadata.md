---
description: supportsSubqueriesInIns-Methode (SQLServerDatabaseMetaData)
title: supportsSubqueriesInIns-Methode (SQLServerDatabaseMetaData) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDatabaseMetaData.supportsSubqueriesInIns
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 77a0b5c0-0d8e-4e08-975f-4eeabb108ab1
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 815430a48bdb36df48703f11899f5edbf3ab2de5
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99189120"
---
# <a name="supportssubqueriesinins-method-sqlserverdatabasemetadata"></a>supportsSubqueriesInIns-Methode (SQLServerDatabaseMetaData)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft ab, ob von dieser Datenbank Unterabfragen in IN-Ausdrücken unterstützt werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean supportsSubqueriesInIns()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 **"true"** unterstützt. Andernfalls lautet der Wert **false**.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese supportsSubqueriesInIns-Methode wird von der supportsSubqueriesInIns-Methode in der java.sql.DatabaseMetaData-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDatabaseMetaData-Methoden](../../../connect/jdbc/reference/sqlserverdatabasemetadata-methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../../../connect/jdbc/reference/sqlserverdatabasemetadata-members.md)   
 [SQLServerDatabaseMetaData-Klasse](../../../connect/jdbc/reference/sqlserverdatabasemetadata-class.md)  
  
  
