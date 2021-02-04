---
description: SQLServerPreparedStatement-Klasse
title: SQLServerPreparedStatement-Klasse | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: a8481c06-fbba-432b-8c69-4f4619c20ad4
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 98d30a2e19ecdc6d5b65a77eb2edc83993c18683
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99172663"
---
# <a name="sqlserverpreparedstatement-class"></a>SQLServerPreparedStatement-Klasse
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Stellt die grundlegende Implementierung der JDBC-Funktion für vorbereitete Anweisungen dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** SQLServerStatement  
  
 **Implementiert** [ISQLServerPreparedStatement](../../../connect/jdbc/reference/isqlserverpreparedstatement-interface.md).  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public class SQLServerPreparedStatement  
```  
  
## <a name="remarks"></a>Bemerkungen  
 SQLServerPreparedStatement stellt Methoden bereit, mit denen Sie Parameter in Form beliebiger nativer Java-Typen und verschiedener Java-Objekttypen angeben können. SQLServerPreparedStatement bereitet anhand der gespeicherten [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] **sp_prepare**-Prozedur Anweisungen vor und verwendet das zurückgegebene Anweisungshandle noch mal für jede nachfolgende Ausführung einer Anweisung, wobei normalerweise verschiedene vom Benutzer bereitgestellte Parameter verwendet werden.  
  
 SQLServerPreparedStatement unterstützt Batchverarbeitung, wobei eine Reihe von vorbereiteten Anweisungen in einem einzelnen Datenbankroundtrip ausgeführt wird, um die Laufzeitleistung zu verbessern.  
  
 Diese Klasse unterstützt das Entpacken in die SQLServerPreparedStatement-Klasse, die Schnittstellen „ISQLServerPreparedStatement“ und „java.sql.PreparedStatement“ und die von SQLServerStatement für das Entpacken unterstützten Klassen und Schnittstellen. Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../../../connect/jdbc/wrappers-and-interfaces.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerPreparedStatement-Elemente](../../../connect/jdbc/reference/sqlserverpreparedstatement-members.md)   
 [API-Referenz für den JDBC-Treiber](../../../connect/jdbc/reference/jdbc-driver-api-reference.md)  
  
  
