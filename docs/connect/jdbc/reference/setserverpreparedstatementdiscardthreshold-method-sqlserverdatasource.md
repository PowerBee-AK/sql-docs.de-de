---
description: setServerPreparedStatementDiscardThreshold-Methode (SQLServerDataSource)
title: setServerPreparedStatementDiscardThreshold Method (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2018
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: ''
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 570b857b9e589fb71d791e47af90acca1927cfc5
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173097"
---
# <a name="setserverpreparedstatementdiscardthreshold-method-sqlserverdatasource"></a>setServerPreparedStatementDiscardThreshold-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Diese Methode legt den Wert der Verbindungseigenschaft serverPreparedStatementDiscardThreshold fest. Mit dieser Einstellung steuern Sie, wie viele ausstehende Aktionen zum Verwerfen vorbereiteter Anweisungen (sp_unprepare) pro Verbindung vorhanden sein dürfen, bevor ein Aufruf zum Bereinigen der ausstehenden Handles auf dem Server ausgeführt wird. Wenn diese Eigenschaft auf „<= 1“ festgelegt ist, werden unprepare-Aktionen sofort nach Abschluss der Prepared Statements ausgeführt. Wenn die Eigenschaft auf „>1“ festgelegt ist, werden diese Aufrufe in einem Batch zusammengefasst, um einen durch zu häufiges Aufrufen von „sp_unprepare“ entstehenden Overhead zu vermeiden.
 
## <a name="syntax"></a>Syntax  
  
```
public void setServerPreparedStatementDiscardThreshold(int enablePrepareOnFirstPreparedStatementCall);  
```  
  
#### <a name="parameters"></a>Parameter  
 *serverPreparedStatementDiscardThreshold*  
  
 Der neue Wert der Verbindungseigenschaft **serverPreparedStatementDiscardThreshold**.  

## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
 
## <a name="remarks"></a>Bemerkungen  
 Diese Methode ist über Version 6.4 und höher des JDCB-Treibers verfügbar.
 
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
