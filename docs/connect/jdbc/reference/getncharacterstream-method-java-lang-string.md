---
description: getNCharacterStream-Methode (java.lang.String)
title: getNCharacterStream(java.lang.String)-Methode | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 45d2695b-0727-419d-8921-a51d6feef0aa
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 7fbf13e4757ccf709d6b6d3151b454bc87b037a3
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99175429"
---
# <a name="getncharacterstream-method-javalangstring"></a>getNCharacterStream-Methode (java.lang.String)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als Readerobjekt ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public final java.io.Reader getNCharacterStream(java.lang.String columnLabel)  
```  
  
#### <a name="parameters"></a>Parameter  
 *columnLabel*  
  
 Eine **Zeichenfolge**, die die Spaltenbezeichnung enthält.  
  
## <a name="return-value"></a>Rückgabewert  
 AReaderobject.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Methode sollte beim Zugriff auf die Parameter **NCHAR**, **NVARCHAR** und **LONGNVARCHAR** verwendet werden.  
  
 Diese getNCharacterStream-Methode wird von der getNCharacterStream-Methode in der java.sql.CallableStatement-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [getNCharacterStream-Methode &#40;SQLServerCallableStatement&#41;](../../../connect/jdbc/reference/getncharacterstream-method-sqlservercallablestatement.md)   
 [SQLServerCallableStatement-Elemente](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)  
  
  
