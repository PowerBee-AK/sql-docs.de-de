---
description: getURL-Methode (SQLServerDataSource)
title: getURL-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.getURL
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: dd0d5d2c-91fe-4b0f-a162-69d898ba176e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: b7a8e5a67d4c99bc525b887df550f70cbd0d8f96
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177644"
---
# <a name="geturl-method-sqlserverdatasource"></a>getURL-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt die URL zurück, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.lang.String getURL()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Ein **String-Objekt**, das die URL enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Aus Sicherheitsgründen sollte das Kennwort nicht in der URL enthalten sein, die an die [setURL](../../../connect/jdbc/reference/seturl-method-sqlserverdatasource.md)-Methode übergeben wird. Der Grund hierfür ist, dass Java-Anwendungsserver von Drittanbietern oft den für die URL-Eigenschaft festgelegten Wert auf der Benutzeroberfläche für die Datenquellenkonfiguration anzeigen. Verwenden Sie stattdessen die [setPassword](../../../connect/jdbc/reference/setpassword-method-sqlserverdatasource.md)-Methode, um den Wert für das Kennwort festzulegen. Java-Anwendungsserver zeigen kein in der Datenquelle festgelegtes Kennwort auf der Konfigurationsbenutzeroberfläche an.  
  
> [!NOTE]  
>  Wird die setURL-Methode nicht vor dem Aufruf der getURL-Methode aufgerufen, wird von getURL der Standardwert „(jdbc:sqlserver://)“ zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
