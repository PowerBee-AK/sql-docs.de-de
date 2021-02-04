---
description: getHostNameInCertificate-Methode (SQLServerDataSource)
title: getHostNameInCertificate-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- getHostNameInCertificate Method (SQLServerDataSource)
apilocation:
- getHostNameInCertificate Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 45ea04e2-9ea5-4171-9136-d09f8a95e128
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 2514fae5914ddf409254531961e4e67765438aac
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99162964"
---
# <a name="gethostnameincertificate-method-sqlserverdatasource"></a>getHostNameInCertificate-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt den Hostnamen zurück, der zum Überprüfen des TLS-Zertifikats (Transport Layer Security), zuvor bekannt als Secure Sockets Layer (SSL), für SQL Server verwendet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.lang.String getHostNameInCertificate()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Eine **Zeichenfolge**, die den Hostnamen oder – sofern kein Wert festgelegt ist – NULL enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Der Hostname dient zum Überprüfen des TLS-/SSL-Zertifikatwerts für SQL Server, wenn die Kommunikationsebene mithilfe von TLS/SSL verschlüsselt wird.  
  
 Ist der Hostname nicht festgelegt, wird von der [getHostNameInCertificate](../../../connect/jdbc/reference/gethostnameincertificate-method-sqlserverdatasource.md)-Methode der Standardwert (NULL) zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
