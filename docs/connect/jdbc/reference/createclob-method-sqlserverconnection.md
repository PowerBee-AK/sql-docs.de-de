---
description: createClob-Methode (SQLServerConnection)
title: createClob-Methode (SQLServerConnection) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 58b0865a-1cde-4046-9761-51e471294023
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0f95d0c8deeb56653c9572b03fc895dfbc8b9010
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99168582"
---
# <a name="createclob-method-sqlserverconnection"></a>createClob-Methode (SQLServerConnection)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Erstellt ein CLOB-Objekt ohne Daten.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.sql.Clob createClob()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Ein Clob-Objekt  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese createClob-Methode wird von der createClob-Methode in der java.sql.Connection-Schnittstelle angegeben.  
  
 Dank dieser Methode wird der [SQLServerBlob-Konstruktor &#40;SQLServerConnection, java.lang.String&#41;](../../../connect/jdbc/reference/sqlserverclob-constructor-sqlserverconnection-java-lang-string.md) nicht mehr benötigt.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerConnection-Elemente](../../../connect/jdbc/reference/sqlserverconnection-members.md)   
 [SQLServerConnection-Klasse](../../../connect/jdbc/reference/sqlserverconnection-class.md)  
  
  
