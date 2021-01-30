---
description: SQLSetScrollOptions-Funktion
title: SQLSetScrollOptions-Funktion | Microsoft-Dokumentation
ms.custom: ''
ms.date: 07/18/2019
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLSetScrollOptions
apilocation:
- sqlsrv32.dll
- odbc32.dll
apitype: dllExport
f1_keywords:
- SQLSetScrollOptions
helpviewer_keywords:
- SQLSetScrollOptions function [ODBC]
ms.assetid: 2a825ba7-7942-4c23-bcdb-c80dc12f8c86
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 69e592350680b4cf3244df823324fb85b8d6153e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99188032"
---
# <a name="sqlsetscrolloptions-function"></a>SQLSetScrollOptions-Funktion
**Konformitäts**  
 Eingeführte Version: ODBC 1,0 Standards Compliance: deprecated  
  
 **Zusammenfassung**  
 In ODBC *3. x* wurde die ODBC 2,0-Funktion **SQLSetScrollOptions** durch Aufrufe von **SQLGetInfo** und **SQLSetStmtAttr** ersetzt.  
  
> [!NOTE]
>  Weitere Informationen dazu, was der Treiber-Manager diese Funktion zuordnet, wenn eine ODBC *2. x* -Anwendung mit einem ODBC *3. x* -Treiber arbeitet, finden Sie unter [Mapping Deprecated Functions](../../../odbc/reference/appendixes/mapping-deprecated-functions.md) in Anhang G: Driver Guidelines for abwärts Compatibility.  
> 
> [!NOTE]
>  Wenn der Treiber-Manager **SQLSetScrollOptions** für eine Anwendung zuordnet, die mit einem ODBC *3. x* -Treiber arbeitet, der **SQLSetScrollOptions** nicht unterstützt, legt der Treiber-Manager die SQL_ROWSET_SIZE Anweisungs Option, nicht das SQL_ATTR_ROW_ARRAY_SIZE Statement-Attribut, auf das *rowsetsize* -Argument in **sqlsetscrolloption** fest. Daher kann **SQLSetScrollOptions** nicht von einer Anwendung verwendet werden, wenn mehrere Zeilen durch einen-Befehl von **SQLFetch** oder **SQLFetchScroll** abgerufen werden. Diese Option kann nur verwendet werden, wenn mehrere Zeilen durch einen **sqlextendebug**-Befehl abgerufen werden.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn Ihre Anwendung unter einem 64-Bit-Betriebssystem ausgeführt wird, finden Sie weitere [Informationen unter ODBC 64-Bit-Informationen](../../../odbc/reference/odbc-64-bit-information.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [ODBC-API-Referenz](../../../odbc/reference/syntax/odbc-api-reference.md)   
 [ODBC-Headerdateien](../../../odbc/reference/install/odbc-header-files.md)
