---
description: setURL-Methode (SQLServerDataSource)
title: setURL-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.setURL
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: bea70100-ac98-4625-8748-ef7cc0b111ea
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0c2af37087028c520d3cfbb7c8b8918009c53d11
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99178439"
---
# <a name="seturl-method-sqlserverdatasource"></a>setURL-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Legt die URL fest, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void setURL(java.lang.String url)  
```  
  
#### <a name="parameters"></a>Parameter  
 *url*  
  
 Ein **String-Objekt**, das die URL enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Aus Sicherheitsgründen sollte das Kennwort nicht in der URL für die setURL-Methode enthalten sein. Der Grund hierfür ist, dass Java-Anwendungsserver von Drittanbietern oft den für die URL-Eigenschaft festgelegten Wert auf der Benutzeroberfläche für die Datenquellenkonfiguration anzeigen. Verwenden Sie stattdessen die [setPassword](../../../connect/jdbc/reference/setpassword-method-sqlserverdatasource.md)-Methode, um den Wert für das Kennwort festzulegen. Java-Anwendungsserver zeigen kein in der Datenquelle festgelegtes Kennwort auf der Konfigurationsbenutzeroberfläche an.  
  
> [!NOTE]  
>  Wird die setURL-Methode nicht vor dem Aufruf der [getURL](../../../connect/jdbc/reference/geturl-method-sqlserverdatasource.md)-Methode aufgerufen, wird von getURL der Standardwert „(jdbc:sqlserver://)“ zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
