---
description: setServerName-Methode (SQLServerDataSource)
title: setServerName-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.setServerName
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 70920828-eda0-4064-be9f-c1e460db8f00
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 086b100bb084fa2c5926f0b7cdade412b19a9bdd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173157"
---
# <a name="setservername-method-sqlserverdatasource"></a>setServerName-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt den Namen des Computers fest, auf dem [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] ausgeführt wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void setServerName(java.lang.String serverName)  
```  
  
#### <a name="parameters"></a>Parameter  
 *serverName*  
  
 Ein **String-Objekt**, das den Servernamen enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Der Servername ist der Hostname des Zielcomputers, auf dem [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] ausgeführt wird. Ist die serverName-Eigenschaft nicht festgelegt, wird von [getServerName](../../../connect/jdbc/reference/getservername-method-sqlserverdatasource.md) der Standardwert (NULL) zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
