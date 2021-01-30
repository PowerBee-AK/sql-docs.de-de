---
description: SQLGetStmtOption-Zuordnung
title: SQLGetStmtOption-Zuordnung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQLGetStmtOption function [ODBC], mapping
- mapping deprecated functions [ODBC], SQLGetStmtOption
ms.assetid: fa599517-3f3e-4dad-a65a-b8596ae3f330
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: aa5d59afe92dbbf6a2e0d2d2cc08abb1a529fe5b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202720"
---
# <a name="sqlgetstmtoption-mapping"></a>SQLGetStmtOption-Zuordnung
Wenn eine Anwendung **SQLGetStmtOption** für einen ODBC *3. x* -Treiber aufruft, der dies nicht unterstützt, wird der Aufruf von  
  
```  
SQLGetStmtOption(hstmt, fOption, pvParam)  
```  
  
 führt zu folgenden Ergebnissen:  
  
-   Wenn " *f Option* " eine ODBC-definierte Anweisungs Option angibt, die eine Zeichenfolge zurückgibt, ruft der Treiber-Manager  
  
    ```  
    SQLGetStmtAttr(StatementHandle, Attribute, ValuePtr, BufferLength, NULL)  
    ```  
  
-   Wenn " *f Option* " eine ODBC-definierte Anweisungs Option angibt, die einen ganzzahligen Wert von 32 Bit zurückgibt, ruft der Treiber-Manager  
  
    ```  
    SQLGetStmtAttr(StatementHandle, Attribute, ValuePtr, 0, NULL)  
    ```  
  
-   Wenn " *f Option* " eine Treiber definierte Anweisungs Option angibt, ruft der Treiber-Manager  
  
    ```  
    SQLGetStmtAttr(StatementHandle, Attribute, ValuePtr, BufferLength, NULL)  
    ```  
  
 In den vorangegangenen drei Fällen wird das *StatementHandle* -Argument auf den Wert in *hstmt* festgelegt, das *Attribut* Argument wird auf den Wert in *fOption* festgelegt, und das *ValuePtr* -Argument wird auf denselben Wert wie *pvParam* festgelegt.  
  
 Für ODBC-definierte Zeichen folgen-Verbindungsoptionen legt der Treiber-Manager das *BufferLength* -Argument im-Befehl auf **SQLGetConnectAttr** auf die vordefinierte maximale Länge (SQL_MAX_OPTION_STRING_LENGTH) fest. für eine nicht-Zeichen folgen-Verbindungs Option wird *BufferLength* auf 0 festgelegt.  
  
 Die Option SQL_GET_BOOKMARK Anweisung wurde in ODBC *3. x* als veraltet markiert. Damit ein ODBC *3. x* -Treiber mit ODBC *2. x* -Anwendungen funktioniert, die SQL_GET_BOOKMARK verwenden, muss er SQL_GET_BOOKMARK unterstützen. Damit ein ODBC *3. x* -Treiber mit ODBC *2. x* -Anwendungen funktioniert, muss er das Festlegen von SQL_USE_BOOKMARKS auf SQL_UB_ON unterstützen und Lesezeichen mit fester Länge verfügbar machen. Wenn ein ODBC *3. x* -Treiber nur Lesezeichen mit variabler Länge, keine Lesezeichen fester Länge unterstützt, muss SQLSTATE HYC00 (optionales Feature nicht implementiert) zurückgegeben werden, wenn eine ODBC *2. x* -Anwendung versucht, SQL_USE_BOOKMARKS auf SQL_UB_ON festzulegen.  
  
 Bei einem ODBC *3. x* -Treiber prüft der Treiber-Manager nicht mehr, ob die *Option* zwischen SQL_STMT_OPT_MIN und SQL_STMT_OPT_MAX liegt oder größer als SQL_CONNECT_OPT_DRVR_START ist. Der Treiber muss dies überprüfen.
