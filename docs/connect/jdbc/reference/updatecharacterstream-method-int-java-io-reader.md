---
description: updateCharacterStream-Methode (int, java.io.Reader)
title: updateCharacterStream-Methode (int, java.io.Reader) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 4dddf885-0482-4776-8e9a-69f6c6270931
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: b27dfd5479005743f39bf092c2608ebdc736f533
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99194233"
---
# <a name="updatecharacterstream-method-int-javaioreader"></a>updateCharacterStream-Methode (int, java.io.Reader)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public void updateCharacterStream(int columnIndex,  
                                  java.io.Reader x)  
```  
  
#### <a name="parameters"></a>Parameter  
 *columnIndex*  
  
 Ein **ganzzahliger** Wert, der den Spaltenindex angibt.  
  
 *x*  
  
 Ein Reader-Objekt  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese updateCharacterStream-Methode wird von der updateCharacterStream-Methode in der java.sql.ResultSet-Schnittstelle angegeben.  
  
 Von dieser Methode werden Unicode-Zeichen aus einem Reader-Objekt an ausgewählte Text- und Binärspalten übergeben. Hierzu zählen alle Textspalten sowie Spalten vom Typ **binary**, **varbinary**, **varbinary(max)** , **image** und **xml**, jedoch keine **udt**-Spalten.  
  
 Die Verwendung dieser Methode für die Datentypen **image**, **text** und **ntext**[!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] kann sich negativ auf die Leistung auswirken.  
  
## <a name="see-also"></a>Weitere Informationen  
 [updateCharacterStream-Methode &#40;SQLServerResultSet&#41;](../../../connect/jdbc/reference/updatecharacterstream-method-sqlserverresultset.md)   
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
