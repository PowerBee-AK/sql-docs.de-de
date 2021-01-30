---
description: SQLInstallTranslator-Funktion
title: Sqlinstalltranslator-Funktion | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLInstallTranslator
apilocation:
- sqlsrv32.dll
apitype: dllExport
f1_keywords:
- SQLInstallTranslator
helpviewer_keywords:
- SQLInstallTranslator function [ODBC]
ms.assetid: 453b21ff-3c2b-4069-8ff7-5c727f062d89
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 40f4c4a5df497c64d081a8d03d1765a4fe5e060a
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99189660"
---
# <a name="sqlinstalltranslator-function"></a>SQLInstallTranslator-Funktion
**Konformitäts**  
 Eingeführte Version: ODBC 2,5, veraltet  
  
 **Zusammenfassung**  
 In ODBC 3,0 wurde **sqlinstalltranslator** durch [sqlinstalltranslatorex](../../../odbc/reference/syntax/sqlinstalltranslatorex-function.md)ersetzt. **Sqlinstalltranslator** -Aufrufe werden **sqlinstalltranslatorex** zugeordnet. Weitere Informationen finden Sie unter **sqlinstalltranslatorex**.  
  
 **Sqlinstalltranslator** gibt false zurück, wenn eine Anwendung Sie im ODBC *3. x* -Treiber-Manager aufruft, wobei das *lpszinffile* -Argument auf einen anderen Wert als NULL festgelegt ist. Die in ODBC *2. x* verwendete ODBC-INF-Datei wird in ODBC *3. x* nicht mehr unterstützt, selbst aus Gründen der Abwärtskompatibilität.
