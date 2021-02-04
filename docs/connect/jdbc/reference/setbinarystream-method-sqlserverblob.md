---
description: setBinaryStream-Methode (SQLServerBlob)
title: setBinaryStream-Methode (SQLServerBlob) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerBlob.setBinaryStream
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: abcec31f-1a60-4765-9725-8cf7e9f1f8ab
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0f72c246530b4f2298af9bf846bad15fd8380d5b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99173862"
---
# <a name="setbinarystream-method-sqlserverblob"></a>setBinaryStream-Methode (SQLServerBlob)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Ruft einen Datenstrom ab, mit dem in den BLOB-Wert geschrieben werden kann.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public java.io.OutputStream setBinaryStream(long pos)  
```  
  
#### <a name="parameters"></a>Parameter  
 *Pos*  
  
 Die Position im BLOB-Wert, an der geschrieben werden soll.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein Ausgabedatenstrom.  
  
## <a name="exceptions"></a>Ausnahmen  
 java.sql.SQLException  
  
## <a name="remarks"></a>Bemerkungen  
 Diese setBinaryStream-Methode wird von der setBinaryStream-Methode in der java.sql.Blob-Schnittstelle angegeben.  
  
 Daten im BLOB werden beginnend mit der angegebenen Position vom Ausgabedatenstrom überschrieben, und sie können die ursprüngliche Länge des BLOB übersteigen. Durch Angeben eines Werts vom Typ Position+1 werden Bytes an die Zeichenfolge angefügt. Durch Weitergeben eines Werts vom Typ Position+2 oder größer (oder null oder weniger) wird ein Positionsfehler ausgelöst.  
  
## <a name="see-also"></a>Weitere Informationen  
 [SQLServerBlob-Methoden](../../../connect/jdbc/reference/sqlserverblob-methods.md)   
 [SQLServerBlob-Elemente](../../../connect/jdbc/reference/sqlserverblob-members.md)   
 [SQLServerBlob-Klasse](../../../connect/jdbc/reference/sqlserverblob-class.md)  
  
  
