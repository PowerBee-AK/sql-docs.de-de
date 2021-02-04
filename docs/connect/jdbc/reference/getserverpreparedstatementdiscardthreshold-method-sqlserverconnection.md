---
description: getServerPreparedStatementDiscardThreshold-Methode (SQLServerConnection)
title: getServerPreparedStatementDiscardThreshold-Methode (SQLServerConnection) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2018
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerConnection.getServerPreparedStatementDiscardThreshold
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: ''
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: ce985283a033c7942b2bca1cb7475a5b1813bcd0
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99175028"
---
# <a name="getserverpreparedstatementdiscardthreshold-method-sqlserverconnection"></a>getServerPreparedStatementDiscardThreshold-Methode (SQLServerConnection)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

 Diese Methode gibt den Wert der Verbindungseigenschaft **serverPreparedStatementDiscardThreshold** zurück. Mit dieser Einstellung steuern Sie, wie viele ausstehende Aktionen zum Verwerfen vorbereiteter Anweisungen (sp_unprepare) pro Verbindung vorhanden sein dürfen, bevor ein Aufruf zum Bereinigen der ausstehenden Handles auf dem Server ausgeführt wird. Wenn diese Einstellung <= 1 ist, werden Aktionen zum Rückgängigmachen der Vorbereitung sofort nach Abschluss der vorbereiteten Anweisung ausgeführt. Wenn die Eigenschaft auf „> 1“ festgelegt ist, werden diese Aufrufe in einem Batch zusammengefasst, um den Aufwand eines zu häufigen Aufrufs von „sp_unprepare“ zu vermeiden. Der Standardwert für diese Option kann durch Aufrufen von getDefaultServerPreparedStatementDiscardThreshold() geändert werden.

## <a name="syntax"></a>Syntax  
  
```  
  
public int getServerPreparedStatementDiscardThreshold()  
```  

## <a name="return-value"></a>Rückgabewert
 Ein **int**-Wert, der den Wert der Verbindungseigenschaft **serverPreparedStatementDiscardThreshold** enthält

## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
 
## <a name="remarks"></a>Bemerkungen  
 Diese Methode ist über Version 6.4 und höher des JDCB-Treibers verfügbar.
 
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerConnection-Elemente](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection-Klasse](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
