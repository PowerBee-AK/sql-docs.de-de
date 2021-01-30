---
description: SQLRemoveDefaultDataSource-Funktion
title: Sqlremovedefaultdatasource-Funktion | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLRemoveDefaultDataSource
apilocation:
- sqlsrv32.dll
apitype: dllExport
f1_keywords:
- SQLRemoveDefaultDataSource
helpviewer_keywords:
- SQLRemoveDefaultDataSource function [ODBC]
ms.assetid: db803266-57df-4864-a41b-901247549c1f
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 326522986785d7e76bc781fa4cc912401f2c237e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99192522"
---
# <a name="sqlremovedefaultdatasource-function"></a>SQLRemoveDefaultDataSource-Funktion
**Konformitäts**  
 Eingeführte Version: ODBC 1,0, veraltet  
  
 **Zusammenfassung**  
 In ODBC 3,0 wurde die **sqlremovedefaultdatasource** -Funktion durch einen-Befehl von [SQLConfigDataSource](../../../odbc/reference/syntax/sqlconfigdatasource-function.md) mit einem *fRequest* -Argument ODBC_REMOVE_DEFAULT_DSN ersetzt. Wenn diese Funktion von einem ODBC 2 *. x* -Installationsprogramm aufgerufen wird, ordnet das ODBC-Installationsprogramm es folgendem **SQLConfigDataSource** -Aufruf zu:  
  
```cpp  
SQLConfigDataSource (NULL, ODBC_REMOVE_DEFAULT_DSN, NULL, NULL)  
```
