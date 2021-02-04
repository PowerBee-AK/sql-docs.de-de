---
description: getXopenStates-Methode (SQLServerDataSource)
title: getXopenStates-Methode (SQLServerDataSource) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerDataSource.getXopenStates
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: de6fdf6b-8345-4490-b35e-7115b61e782e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 115ceb9c00c9d5b9e8871724786b4adcec1b89dd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99177562"
---
# <a name="getxopenstates-method-sqlserverdatasource"></a>getXopenStates-Methode (SQLServerDataSource)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt einen Wert vom Typ **boolean** zurück, mit dem angegeben wird, ob das Konvertieren von SQL-Status in XOPEN-kompatible Status aktiviert ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public boolean getXopenStates()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 **TRUE**, wenn das Konvertieren von SQL-Status zu XOPEN-kompatiblen Status aktiviert ist. Andernfalls lautet der Wert **false**.  
  
## <a name="remarks"></a>Bemerkungen  
 Ist die xopenStates-Eigenschaft auf **true** festgelegt, werden SQL-Status von [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)] in XOPEN-kompatible Status konvertiert. Durch den Standardwert **false** werden vom JDBC-Treiber SQL 99-Statuscodes zurückgegeben. Ist die xopenStates-Eigenschaft nicht festgelegt, wird von der getXopenStates-Methode der Standardwert **false** zurückgegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerDataSource-Elemente](../../../connect/jdbc/reference/sqlserverdatasource-members.md)   
 [SQLServerDataSource-Klasse](../../../connect/jdbc/reference/sqlserverdatasource-class.md)  
  
  
