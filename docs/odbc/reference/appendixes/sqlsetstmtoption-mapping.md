---
description: SQLSetStmtOption-Zuordnung
title: SQLSetStmtOption-Zuordnung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- mapping deprecated functions [ODBC], SQLSetStmtOption
- SQLSetStmtOption function [ODBC], mapping
ms.assetid: 6a9921aa-8a53-4668-9b13-87164062f1e5
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 8907de6d6ac80737ba0bb47ca3c6954a482c857f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202582"
---
# <a name="sqlsetstmtoption-mapping"></a>SQLSetStmtOption-Zuordnung
Wenn eine Anwendung **SQLSetStmtOption** über einen ODBC *3. x* -Treiber aufruft, wird der Aufruf von  
  
```  
SQLSetStmtOption(StatementHandle, fOption, vParam)  
```  
  
 führt zu folgenden Ergebnissen:  
  
-   Wenn " *f Option* " ein ODBC-definiertes Anweisungs Attribut angibt, das eine Zeichenfolge ist, ruft der Treiber-Manager  
  
    ```  
    SQLSetStmtAttr(StatementHandle, fOption, ValuePtr, SQL_NTS)  
    ```  
  
-   Wenn " *f Option* " ein ODBC-definiertes Anweisungs Attribut angibt, das einen ganzzahligen Wert von 32 Bit zurückgibt, ruft der Treiber-Manager  
  
    ```  
    SQLSetStmtAttr(StatementHandle, fOption, ValuePtr, 0)  
    ```  
  
-   Wenn " *f Option* " ein Treiber definiertes Anweisungs Attribut angibt, ruft der Treiber-Manager  
  
    ```  
    SQLSetStmtAttr(StatementHandle, fOption, ValuePtr, BufferLength)  
    ```  
  
 In den vorangegangenen drei Fällen wird das **StatementHandle** -Argument auf den Wert in *hstmt* festgelegt, das *Attribut* Argument wird auf den Wert in *fOption* festgelegt, und das *ValuePtr* -Argument wird auf den Wert *vParam* festgelegt.  
  
 Da der Treiber-Manager nicht weiß, ob das Treiber definierte Anweisungs Attribut eine Zeichenfolge oder einen ganzzahligen ganzzahligen Wert von 32 benötigt, muss ein gültiger Wert für das *StringLength* -Argument von **SQLSetStmtAttr** übergeben werden. Wenn der Treiber eine spezielle Semantik für Treiber definierte Anweisungs Attribute definiert hat und mithilfe von **SQLSetStmtOption** aufgerufen werden muss, muss **SQLSetStmtOption** unterstützt werden.  
  
 Wenn eine Anwendung **SQLSetStmtOption** aufruft, um eine Treiber spezifische Anweisungs Option in einem ODBC *3. x* -Treiber festzulegen, und die-Option in einer ODBC *2. x* -Version des Treibers definiert wurde, sollte für die-Option im ODBC *3. x* -Treiber eine neue Manifest-Konstante definiert werden. Wenn die alte Manifest-Konstante beim Aufrufen von **SQLSetStmtOption** verwendet wird, ruft der Treiber-Manager **SQLSetStmtAttr** auf, wobei das *StringLength* -Argument auf 0 festgelegt ist.  
  
 Wenn eine Anwendung **SQLSetStmtAttr** aufruft, um SQL_ATTR_USE_BOOKMARKS auf SQL_UB_ON in einem ODBC *3. x* -Treiber festzulegen, wird das SQL_ATTR_USE_BOOKMARKS-Anweisungs Attribut auf SQL_UB_FIXED festgelegt. SQL_UB_ON ist dieselbe Konstante wie SQL_UB_FIXED. Der Treiber-Manager übergibt SQL_UB_FIXED an den Treiber. SQL_UB_FIXED ist in ODBC *3. x* veraltet, aber ein ODBC *3. x* -Treiber muss ihn implementieren, um mit ODBC *2. x* -Anwendungen arbeiten zu können, die Lesezeichen mit fester Länge verwenden.  
  
 Bei einem ODBC *3. x* -Treiber prüft der Treiber-Manager nicht mehr, ob die *Option* zwischen SQL_STMT_OPT_MIN und SQL_STMT_OPT_MAX liegt oder größer als SQL_CONNECT_OPT_DRVR_START ist.
