---
description: setTransactionTimeout-Methode (SQLServerXAResource)
title: setTransactionTimeout-Methode (SQLServerXAResource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerXAResource.setTransactionTimeout
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 38bf4a1a-6ad3-437c-b9ed-8792ab6dde7e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 6cfd7379a9315910b0822072268791a6c37cbcf0
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99172981"
---
# <a name="settransactiontimeout-method-sqlserverxaresource"></a>setTransactionTimeout-Methode (SQLServerXAResource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt den aktuellen Transaktionstimeoutwert für das [SQLServerXAResource](../../../connect/jdbc/reference/sqlserverxaresource-class.md)-Objekt fest.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean setTransactionTimeout(int seconds)  
```  
  
#### <a name="parameters"></a>Parameter  
 *Sekunden*  
  
 Ein **int**-Wert  
  
## <a name="return-value"></a>Rückgabewert  
 **TRUE**, wenn das Timeout erfolgreich festgelegt wurde. Andernfalls lautet der Wert **false**.  
  
## <a name="exceptions"></a>Ausnahmen  
 javax.transaction.xa.XAException  
  
## <a name="remarks"></a>Bemerkungen  
 Diese setTransactionTimeout-Methode wird von der setTransactionTimeout-Methode in der javax.transaction.xa.XAResource-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerXAResource-Methoden](../../../connect/jdbc/reference/sqlserverxaresource-methods.md)   
 [SQLServerXAResource-Elemente](../../../connect/jdbc/reference/sqlserverxaresource-members.md)   
 [SQLServerXAResource-Klasse](../../../connect/jdbc/reference/sqlserverxaresource-class.md)  
  
  
