---
description: getCharacterStream-Methode (long, long) (SQLServerNClob)
title: getCharacterStream-Methode (long, long) (SQLServerNClob) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 5a8028bc-c877-4668-b662-0746d462040e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: dea79fc0a80221462e3c01a9c3b9ca625b77dd86
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99168089"
---
# <a name="getcharacterstream-method-long-long-sqlservernclob"></a>getCharacterStream-Methode (long, long) (SQLServerNClob)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft die **NCLOB**-Daten als **Reader**-Objekt oder als Zeichendatenstrom mit einer angegebenen Position und Länge ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.io.Reader getCharacterStream(long pos,  
                                  long length)  
```  
  
#### <a name="parameters"></a>Parameter  
 *pos*  
  
 Ein Wert vom Typ **long**, mit dem das Offset zum ersten Zeichen des abzurufenden Teilwerts angegeben wird.  
  
 *length*  
  
 Ein Wert vom Typ **long**, mit dem die Länge (in Zeichen) des abzurufenden Teilwerts angegeben wird.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein Readerobjekt, das die **NCLOB**-Daten enthält.  
  
## <a name="exceptions"></a>Ausnahmen  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Bemerkungen  
 Diese getCharacterStream-Methode wird von der getCharacterStream-Methode in der java.sql.NClob-Schnittstelle angegeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [getCharacterStream-Methode &#40;SQLServerNClob&#41;](../../../connect/jdbc/reference/getcharacterstream-method-sqlservernclob.md)   
 [SQLServerNClob-Methoden](../../../connect/jdbc/reference/sqlservernclob-methods.md)   
 [SQLServerNClob-Elemente](../../../connect/jdbc/reference/sqlservernclob-members.md)   
 [SQLServerNClob-Klasse](../../../connect/jdbc/reference/sqlservernclob-class.md)  
  
  
