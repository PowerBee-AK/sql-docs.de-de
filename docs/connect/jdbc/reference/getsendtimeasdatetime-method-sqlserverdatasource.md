---
description: getSendTimeAsDatetime-Methode (SQLServerDataSource)
title: Methode „getSendTimeAsDatetime“ (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 02287122-5dc1-455d-987f-95fd9a69d503
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: ba9fd31fdbc5626fc3baa81c853bc78ea2a81abc
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99175067"
---
# <a name="getsendtimeasdatetime-method-sqlserverdatasource"></a>getSendTimeAsDatetime-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Diese Methode wurde im JDBC-Treiber 3.0 für [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] hinzugefügt.  
  
 Gibt die Einstellung der **sendTimeAsDatetime**-Verbindungseigenschaft zurück  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean getSendTimeAsDatetime();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn **TRUE**, werden java.sql.Time-Werte in  als [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] **datetime**-Werte an den Server gesendet. Wenn **FALSE**, werden java.sql.Time-Werte in  als [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] **time**-Werte an den Server gesendet.  
  
## <a name="remarks"></a>Bemerkungen  
 Weitere Informationen zur [sendTimeAsDatetime](../../../connect/jdbc/setting-the-connection-properties.md)-Verbindungseigenschaft finden Sie unter **Festlegen von Verbindungseigenschaften**.  
  
 Mit [SQLServerDataSource.setSendTimeAsDatetime](../../../connect/jdbc/reference/setsendtimeasdatetime-method-sqlserverdatasource.md) können Sie die Verbindungseigenschaft **sendTimeAsDatetime** programmgesteuert festlegen.  
  
 Weitere Informationen finden Sie unter [Configuring How java.sql.Time Values are Sent to the Server (Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden)](../../../connect/jdbc/configuring-how-java-sql-time-values-are-sent-to-the-server.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
