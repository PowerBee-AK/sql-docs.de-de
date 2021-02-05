---
description: SQLServerException-Klasse
title: SQLServerException-Klasse | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: af5ef257-7cf6-4db3-b1ee-07d22d82bef1
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 706312c690052a89e2243c2714a151a56c4f200b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99178229"
---
# <a name="sqlserverexception-class"></a>SQLServerException-Klasse
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Stell die fehlerhafte oder unvollständige Ausführung einer SQL-Anweisung dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.SQLException  
  
 **Implementiert:** java.io.Serializable  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public final class SQLServerException  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Die SQLServerException-Klasse behandelt sowohl SQL-92- als auch XOPEN-Statuscodes. Diese verwenden eine vom Benutzer angegebene Verbindungseigenschaft und sind daher wechselbar. Ausnahmen werden in die angegebenen offenen Protokolldateien geschrieben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerException-Elemente](../../../connect/jdbc/reference/sqlserverexception-members.md)   
 [API-Referenz für den JDBC-Treiber](../../../connect/jdbc/reference/jdbc-driver-api-reference.md)  
  
  
