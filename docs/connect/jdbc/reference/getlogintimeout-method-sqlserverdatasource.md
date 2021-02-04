---
description: getLoginTimeout-Methode (SQLServerDataSource)
title: getLoginTimeout-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.getLoginTimeout
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 316f067c-9e08-456a-af19-b80b0bbd4a5c
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0748b46e99113e80266379361ed403815621feec
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99162887"
---
# <a name="getlogintimeout-method-sqlserverdatasource"></a>getLoginTimeout-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt die Anzahl von Sekunden zurück, die vom [SQLServerDataSource](../../../connect/jdbc/reference/sqlserverdatasource-class.md)-Objekt bei der Verbindungsherstellung gewartet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public int getLoginTimeout()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Ein Wert vom Typ **int** zum Darstellen der Wartedauer in Sekunden.  
  
## <a name="remarks"></a>Hinweise  
 Wird von der Anwendung kein expliziter Timeoutwert angegeben, werden von dieser Methode standardmäßig 15 Sekunden zurückgegeben.  
  
 Diese getLoginTimeout-Methode wird von der getLoginTimeout-Methode in der javax.sql.DataSource-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
