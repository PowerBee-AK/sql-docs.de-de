---
description: getStatementPoolingCacheSize-Methode (SQLServerDataSource)
title: getStatementPoolingCacheSize-Methode (SQLServerDataSource) | Microsoft-Dokumentation
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
ms.openlocfilehash: 4f180e89179909b355220aa3d453ee2a3e213ab4
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99162207"
---
# <a name="getstatementpoolingcachesize-method-sqlserverdatasource"></a>getStatementPoolingCacheSize-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Diese Methode gibt den Wert der Verbindungseigenschaft **statementPoolingCacheSize** zurück. Sie gibt die Größe des Prepared Statement-Caches für diese Verbindung zurück. 0 (null) bedeutet, dass das Zwischenspeichern nicht aktiviert ist.
  
## <a name="syntax"></a>Syntax  
  
```
public boolean getStatementPoolingCacheSize();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Dies ist der Wert **int** der Verbindungseigenschaft **statementPoolingCacheSize**.  

## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
 
## <a name="remarks"></a>Bemerkungen  
 Diese Methode ist über Version 6.4 und höher des JDCB-Treibers verfügbar.
 
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
