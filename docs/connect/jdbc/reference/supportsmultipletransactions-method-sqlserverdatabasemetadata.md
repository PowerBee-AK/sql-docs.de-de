---
description: supportsMultipleTransactions-Methode (SQLServerDatabaseMetaData)
title: supportsMultipleTransactions-Methode (SQLServerDatabaseMetaData) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDatabaseMetaData.supportsMultipleTransactions
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 34ff8dcb-5487-46d1-a4c1-25e33eb3eee4
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f6f5a88e1c239ca755dd98a1a61f6a6633a3c27e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99185827"
---
# <a name="supportsmultipletransactions-method-sqlserverdatabasemetadata"></a>supportsMultipleTransactions-Methode (SQLServerDatabaseMetaData)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft ab, ob bei dieser Datenbank gleichzeitig mehrere Transaktionen für unterschiedliche Verbindungen geöffnet sein können.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean supportsMultipleTransactions()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 **"true"** unterstützt. Andernfalls lautet der Wert **false**.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese supportsMultipleTransactions-Methode wird von der supportsMultipleTransactions-Methode in der java.sql.DatabaseMetaData-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDatabaseMetaData-Methoden](../../../connect/jdbc/reference/sqlserverdatabasemetadata-methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../../../connect/jdbc/reference/sqlserverdatabasemetadata-members.md)   
 [SQLServerDatabaseMetaData-Klasse](../../../connect/jdbc/reference/sqlserverdatabasemetadata-class.md)  
  
  
