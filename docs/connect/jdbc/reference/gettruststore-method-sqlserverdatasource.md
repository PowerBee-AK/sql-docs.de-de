---
description: getTrustStore-Methode (SQLServerDataSource)
title: getTrustStore-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- getTrustStore Method (SQLServerDataSource)
apilocation:
- getTrustStore Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 8f5850e4-8627-49a8-ba0e-b1f4014322a5
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 71365a85690c74025b6d807eb4def767156996cd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99165465"
---
# <a name="gettruststore-method-sqlserverdatasource"></a>getTrustStore-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt den Pfad (einschließlich Dateiname) zur trustStore-Zertifikatsdatei zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.lang.String getTrustStore()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Eine **Zeichenfolge** mit dem Pfad (einschließlich Dateiname) zur trustStore-Zertifikatsdatei, oder NULL, wenn kein Wert festgelegt wurde.  
  
## <a name="remarks"></a>Hinweise  
 Ist die trustStore-Eigenschaft nicht festgelegt, wird von der [getTrustStore](../../../connect/jdbc/reference/gettruststore-method-sqlserverdatasource.md)-Methode NULL zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
