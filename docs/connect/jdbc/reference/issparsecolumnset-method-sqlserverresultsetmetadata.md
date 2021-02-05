---
description: isSparseColumnSet-Methode (SQLServerResultSetMetaData)
title: isSparseColumnSet-Methode (SQLServerResultSetMetaData) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: ac363670-78ae-49f1-aeda-4fba3329a258
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 7d84f7d53f3b8040e2d126eb6166bc211d97a770
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177210"
---
# <a name="issparsecolumnset-method-sqlserverresultsetmetadata"></a>isSparseColumnSet-Methode (SQLServerResultSetMetaData)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt an, ob eine Spalte in einem Resultset ein Satz von Sparsespalten ist.  
  
## <a name="syntax"></a>Syntax  
  
```scr  
public boolean isSparseColumnSet(int column)  
```  
  
#### <a name="parameters"></a>Parameter  
 *column*  
  
 Der Index der Spalte (mit der Basis eins).  
  
## <a name="return-value"></a>Rückgabewert  
 **TRUE**, wenn es sich bei einer Spalte in einem Resultset um einen Sparsespaltensatz handelt; andernfalls **FALSE**  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Methode ruft keine Informationen aus der Datenbank ab.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerResultSetMetaData-Methoden](../../../connect/jdbc/reference/sqlserverresultsetmetadata-methods.md)   
 [SQLServerResultSetMetaData-Elemente](../../../connect/jdbc/reference/sqlserverresultsetmetadata-members.md)   
 [SQLServerResultSetMetaData-Klasse](../../../connect/jdbc/reference/sqlserverresultsetmetadata-class.md)  
  
  
