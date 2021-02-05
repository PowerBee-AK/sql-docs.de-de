---
description: SQLServerDataSourceObjectFactory-Klasse
title: SQLServerDataSourceObjectFactory-Klasse | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: b616632b-5987-470d-b36c-b22fa9213145
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f4545776ff08e1f2fdd1760e652770a34733f058
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99178276"
---
# <a name="sqlserverdatasourceobjectfactory-class"></a>SQLServerDataSourceObjectFactory-Klasse
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Stellt ein Objektfactory zum Materialisieren von Datenquellen aus der JNDI (Java Naming and Directory Interface) dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.lang.Object  
  
 **Implementiert:** javax.naming.spi.ObjectFactory  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public class SQLServerDataSourceObjectFactory  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Methode wird von allen Datenquellenklassen geerbt. Diese Klasse, von der ein ObjectFactory-Objekt implementiert wird, wird von [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] als Teil der Unterstützung der Referenceable-Schnittstelle verfügbar gemacht. Von Java-Anwendungsservern wird getReference für Datenquellenklassen aufgerufen, wodurch ein Reference-Objekt erstellt wird, von dem der Klassenname intern als Klassenfactory verwendet wird.  
  
 Wenn das Reference-Objekt vom Java-Anwendungsserver dereferenziert werden muss, wird eine Instanz des SQLServerDataSourceObjectFactory-Objekts erstellt und die [getObjectInstance](../../../connect/jdbc/reference/getobjectinstance-method-sqlserverdatasourceobjectfactory.md)-Methode aufgerufen, um die Datenquellinstanz abzurufen. Dabei wird das Reference-Objekt übergeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSourceObjectFactory-Elemente](../../../connect/jdbc/reference/sqlserverdatasourceobjectfactory-members.md)   
 [API-Referenz für den JDBC-Treiber](../../../connect/jdbc/reference/jdbc-driver-api-reference.md)  
  
  
