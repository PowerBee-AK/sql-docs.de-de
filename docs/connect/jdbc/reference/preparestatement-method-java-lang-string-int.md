---
description: prepareStatement-Methode (java.lang.String)
title: prepareStatement Method (java.lang.String) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 02/07/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLServerConnection.prepareStatement (java.lang.String)
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: e825765c-eb55-4800-951b-f3495da36641
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 13e38bd96fa9fe6215b664bbe90536fe967dd06f
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100045430"
---
# <a name="preparestatement-method-javalangstring"></a>prepareStatement-Methode (java.lang.String)

Erstellt ein [SQLServerPreparedStatement](./sqlserverpreparedstatement-class.md)-Objekt zum Senden von parametrisierten SQL-Anweisungen an die Datenbank.

## <a name="syntax"></a>Syntax

```
public java.sql.PreparedStatement prepareStatement(java.lang.String sql)
```

#### <a name="parameters"></a>Parameter
*sql*

Eine **Zeichenfolge**, die eine SQL-Anweisung enthält.

## <a name="return-value"></a>Rückgabewert
Dies ist ein PreparedStatement-Objekt.

## <a name="exceptions"></a>Ausnahmen  
[SQLServerException](./sqlserverexception-class.md)

## <a name="remarks"></a>Bemerkungen
Diese prepareStatement-Methode wird von der prepareStatement-Methode in der java.sql.Connection-Schnittstelle angegeben.

## <a name="see-also"></a>Weitere Informationen

[prepareStatement-Methode &#40;SQLServerConnection&#41;](./preparestatement-method-sqlserverconnection.md)

[SQLServerConnection-Elemente](./sqlserverconnection-members.md)

[SQLServerConnection-Klasse](./sqlserverconnection-class.md)
