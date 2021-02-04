---
description: getEnablePrepareOnFirstPreparedStatementCall-Methode (SQLServerDataSource)
title: getEnablePrepareOnFirstPreparedStatementCall-Methode (SQLServerDataSource)
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
ms.openlocfilehash: 266a9094e55c8ea239bf3a9997aa684042c84b76
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99163072"
---
# <a name="getenableprepareonfirstpreparedstatementcall-method-sqlserverdatasource"></a>getEnablePrepareOnFirstPreparedStatementCall-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Diese Methode gibt den Wert der Verbindungseigenschaft **enablePrepareOnFirstPreparedStatementCall** zurück. Gibt diese Konfiguration FALSE zurück, ruft die erste Ausführung einer vorbereiteten Anweisung sp_executesql auf und bereitet keine Anweisung vor. Sobald die zweite Ausführung erfolgt, ruft diese sp_prepexec auf und richtet tatsächlich ein vorbereitetes Anweisungshandle ein. Bei den folgenden Ausführungen wird sp_execute aufgerufen. Dadurch ist „sp_unprepare“ nicht mehr für den Abschluss einer vorbereiteten Anweisung erforderlich, falls diese nur einmal ausgeführt wird. 
  
## <a name="syntax"></a>Syntax  
  
```
public boolean getEnablePrepareOnFirstPreparedStatementCall();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt den **booleschen** Wert der Verbindungseigenschaft **enablePrepareOnFirstPreparedStatementCall** an  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
 
## <a name="remarks"></a>Bemerkungen  
 Diese Methode ist über Version 6.4 und höher des JDCB-Treibers verfügbar.
 
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
