---
description: setDisableStatementPooling-Methode (SQLServerDataSource)
title: setDisableStatementPooling-Methode (SQLServerDataSource) | Microsoft-Dokumentation
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
ms.openlocfilehash: 2aab090785dda921cb1061f5ab59e90136fc3b3d
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173501"
---
# <a name="setdisablestatementpooling-method-sqlserverdatasource"></a>setDisableStatementPooling-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Diese Methode legt den Wert der Verbindungseigenschaft **disableStatementPooling** fest. Wenn FALSE, können Sie das Anweisungspooling zusammen mit statementPoolingCacheSize value > 0 verwenden.  

## <a name="syntax"></a>Syntax  
  
```
public void setDisableStatementPooling(boolean disableStatementPooling);  
```  
  
#### <a name="parameters"></a>Parameter  
 *disableStatementPooling*  
  
 Der neue Wert der Verbindungseigenschaft **disableStatementPooling**  

## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
 
## <a name="remarks"></a>Bemerkungen  
 Diese Methode ist über Version 6.4 und höher des JDCB-Treibers verfügbar.
 
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
