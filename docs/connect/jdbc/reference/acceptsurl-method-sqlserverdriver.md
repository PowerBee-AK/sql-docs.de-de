---
description: acceptsURL-Methode (SQLServerDriver)
title: acceptsURL-Methode (SQLServerDriver) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDriver.acceptsURL
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: fc744566-7191-4b15-9f76-b4b8087fb14a
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0269ab57fb0be55f57c8fb97c5d39f6cda37359e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99168743"
---
# <a name="acceptsurl-method-sqlserverdriver"></a>acceptsURL-Methode (SQLServerDriver)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Überprüft, ob die angegebene URL gültig ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean acceptsURL(java.lang.String url)  
```  
  
#### <a name="parameters"></a>Parameter  
 *url*  
  
 Ein **Zeichenfolgenwert** mit der URL, die zum Herstellen einer Verbindung mit der Datenbank verwendet wird.  
  
## <a name="return-value"></a>Rückgabewert  
 Der Wert ist **true**, wenn die angegebene URL gültig ist. Andernfalls lautet der Wert **false**.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese acceptsURL-Methode wird von der acceptsURL-Methode in der java.sql.Driver-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDriver-Methoden](../../../connect/jdbc/reference/sqlserverdriver-methods.md)   
 [SQLServerDriver-Elemente](../../../connect/jdbc/reference/sqlserverdriver-members.md)   
 [SQLServerDriver-Klasse](../../../connect/jdbc/reference/sqlserverdriver-class.md)  
  
  
