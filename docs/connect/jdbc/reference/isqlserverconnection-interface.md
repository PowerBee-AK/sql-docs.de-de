---
description: ISQLServerConnection-Schnittstelle
title: ISQLServerConnection-Schnittstelle | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 031c01e2-2c65-4fe4-9700-fdbcc7a39f30
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 5749dbc228625d28176138eb56606eff930fc0d6
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177368"
---
# <a name="isqlserverconnection-interface"></a>ISQLServerConnection-Schnittstelle
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Stellt eine JDBC-Verbindung mit einer [!INCLUDE[msCoName](../../../includes/msconame_md.md)][!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)]-Datenbank dar. Diese Schnittstelle wurde im JDBC-Treiber 3.0 für [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.Connection  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public interface ISQLServerConnection  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Schnittstelle wird von der Klasse [SQLServerConnection](../../../connect/jdbc/reference/sqlserverconnection-class.md) implementiert.  
  
 Diese Schnittstelle macht das folgende [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)]-spezifische Feld verfügbar:  
  
|Feld|Weitere Informationen finden Sie unter|  
|-----------|-------------------------------|  
|öffentliches final static int TRANSACTION_SNAPSHOT|[TRANSACTION_SNAPSHOT](../../../connect/jdbc/reference/transaction-snapshot-field-sqlserverconnection.md)|  
|öffentliche UUID getClientConnectionId()|[getClientConnectionID()](../../../connect/jdbc/reference/getclientconnectionid-method-sqlserverconnection.md)|  
  
## <a name="see-also"></a>Weitere Informationen  
 [API-Referenz für den JDBC-Treiber](../../../connect/jdbc/reference/jdbc-driver-api-reference.md)  
  
  
