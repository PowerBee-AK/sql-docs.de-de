---
description: SQLSetParam-Zuordnung
title: SQLSetParam-Zuordnung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- mapping deprecated functions [ODBC], SQLSetParam
- SQLSetParam function [ODBC], mapping
ms.assetid: 022dfbc0-8d18-4c35-8a28-d9eb16063188
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 6e2488c689a4da1152e115017287274252c6b405
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202629"
---
# <a name="sqlsetparam-mapping"></a>SQLSetParam-Zuordnung
**SQLSetParam** wird weiterhin auf **SQLBindParameter** wie in ODBC 2 zugeordnet. *x*. Obwohl es konzeptionell mit **SQLBindParam** vergleichbar ist, ordnet der Treiber-Manager **SQLSetParam** nicht zu **SQLBindParam** zu. Dies liegt daran, dass bestimmte vorhandene ODBC 2-. *x* -Treiber verwenden den besonderen Wert von *BufferLength* (SQL_SETPARAM_VALUE_MAX), den der Treiber-Manager generiert, wenn er **SQLSetParam** Top von **SQLBindParameter** zuordnet, um zu bestimmen, wann er von 1 aufgerufen wird. *x* ODBC-Anwendung.  
  
 Ein-Rückruf  
  
```  
SQLSetParam(hstmt, ipar, fCType, fSqlType, cbColDef, ibScale, rgbValue, pcbValue)  
```  
  
 führt zu folgendem:  
  
```  
SQLBindParameter(StatementHandle, ParameterNumber, SQL_PARAM_INPUT_OUTPUT, ValueType, ParameterType, ColumnSize, DecimalDigits, ParameterValuePtr, SQL_SETPARAM_VALUE_MAX, StrLen_or_IndPtr)  
```
