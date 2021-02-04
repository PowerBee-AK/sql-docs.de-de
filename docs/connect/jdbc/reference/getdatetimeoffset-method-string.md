---
description: getDateTimeOffset-Methode (Zeichenfolge)
title: getDateTimeOffset-Methode (Zeichenfolge) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: fedb1d75-0c3d-4eb3-ae65-da0e153265cc
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f4f7fd5cfba40ccd28c894e77ea823ae1252cf74
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99163164"
---
# <a name="getdatetimeoffset-method-string"></a>getDateTimeOffset-Methode (Zeichenfolge)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Diese Methode wurde im JDBC-Treiber 3.0 für [!INCLUDE[msCoName](../../../includes/msconame_md.md)][!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] hinzugefügt.  
  
 Ruft den Wert der angegebenen Spalte unter Berücksichtigung des Parameterindexes als [DateTimeOffset-Klassenobjekt](../../../connect/jdbc/reference/datetimeoffset-class.md) in Java ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public microsoft.sql.DateTimeOffset getDateTimeOffset(String sCol)  
```  
  
#### <a name="parameters"></a>Parameter  
 *sCol*  
  
 Der Name eines Parameters.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein [DateTimeOffset-Klassenobjekt](../../../connect/jdbc/reference/datetimeoffset-class.md)  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Sie können mit [SQLServerCallableStatement.setDateTimeOffset](../../../connect/jdbc/reference/setdatetimeoffset-method-sqlservercallablestatement.md) einen Parameterwert der Klasse [DateTimeOffset](../../../connect/jdbc/reference/datetimeoffset-class.md) festlegen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [getDateTimeOffset-Methode &#40;SQLServerCallableStatement&#41;](../../../connect/jdbc/reference/getdatetimeoffset-method-sqlservercallablestatement.md)   
 [SQLServerCallableStatement-Elemente](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)   
 [SQLServerCallableStatement-Klasse](../../../connect/jdbc/reference/sqlservercallablestatement-class.md)  
  
  
