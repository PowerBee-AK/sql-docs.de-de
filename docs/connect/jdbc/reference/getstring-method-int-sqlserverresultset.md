---
description: getString-Methode (int) (SQLServerResultSet)
title: getString-Methode (int) (SQLServerResultSet) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerResultSet.getString (int)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: bfa493c4-fe07-449b-b4d0-384e1a1fce48
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d679ea82b07c7df4aef09b47c7cc74e537a94070
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99174971"
---
# <a name="getstring-method-int-sqlserverresultset"></a>getString-Methode (int) (SQLServerResultSet)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../../../connect/jdbc/reference/sqlserverresultset-class.md)-Objekts als **String-Objekt** in der Programmiersprache Java ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.lang.String getString(int columnIndex)  
```  
  
#### <a name="parameters"></a>Parameter  
 *columnIndex*  
  
 Ein **ganzzahliger** Wert, der den Spaltenindex angibt.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein **String-Wert**.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese getString-Methode wird von der getString-Methode in der java.sql.ResultSet-Schnittstelle angegeben.  
  
 Alle Spalten in [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] können als String-Objekt zurückgegeben werden. D.h., es kann eine **String-Darstellung** aller zahlen- und zeichenfolgenbasierter Typen und eine hexadezimale String-Darstellung binärer Spalten wie binary, varbinary, varbinary(max), image, timestamp oder uniqueidentifier zurückgegeben werden.  
  
 Den Speicherort berücksichtigende Typen wie „money“, „smallmoney“, „datetime“, „smalldatetime“, „float“, „real“, „decimal“ oder „numeric“ geben für den zugrunde liegenden Wert des Typs das kanonische toString()-Format zurück.  
  
 Benutzerdefinierte Typen werden als hexadezimale **String-Werte** zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [getString-Methode &#40;SQLServerResultSet&#41;](../../../connect/jdbc/reference/getstring-method-sqlserverresultset.md)   
 [SQLServerResultSet-Elemente](../../../connect/jdbc/reference/sqlserverresultset-members.md)   
 [SQLServerResultSet-Klasse](../../../connect/jdbc/reference/sqlserverresultset-class.md)  
  
  
