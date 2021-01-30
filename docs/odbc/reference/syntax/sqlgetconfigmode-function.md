---
description: SQLGetConfigMode-Funktion
title: Sqlgetconfigmode-Funktion | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- SQLGetConfigMode
apilocation:
- sqlsrv32.dll
apitype: dllExport
f1_keywords:
- SQLGetConfigMode
helpviewer_keywords:
- SQLGetConfigMode function [ODBC]
ms.assetid: b96ab3b8-08d5-4fea-9ffe-e03043efbf2d
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0ccd703f6fd8c7b80dec575d85e44f2c955ea669
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99203470"
---
# <a name="sqlgetconfigmode-function"></a>SQLGetConfigMode-Funktion
**Konformitäts**  
 Eingeführte Version: ODBC 3,0  
  
 **Zusammenfassung**  
 **Sqlgetconfigmode** Ruft den Konfigurations Modus ab, der angibt, wo sich der Odbc.ini Eintrag mit den DSN-Werten in den Systeminformationen befindet.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
  
BOOL SQLGetConfigMode(  
     UWORD *   pwConfigMode);  
```  
  
## <a name="arguments"></a>Argumente  
 *pwconfigmode*  
 Ausgeben Zeiger auf den Puffer, der den Konfigurations Modus enthält. (Siehe "Kommentare") Der Wert in " *\* pwconfigmode* " kann wie folgt lauten:  
  
 ODBC_USER_DSN  
  
 ODBC_SYSTEM_DSN  
  
 ODBC_BOTH_DSN  
  
## <a name="returns"></a>Gibt zurück  
 Die Funktion gibt true zurück, wenn Sie erfolgreich ist, andernfalls false.  
  
## <a name="diagnostics"></a>Diagnose  
 Wenn **sqlgetconfigmode** false zurückgibt, kann ein zugeordneter Getter *\* rorcode* -Wert durch Aufrufen von **sqlinstallererror** abgerufen werden. In der folgenden Tabelle sind die " *\* pferrorcode* "-Werte aufgelistet, die von " **sqlinstallererror** " zurückgegeben werden können. Diese werden im Kontext dieser Funktion erläutert.  
  
|*\*pferrorcode*|Fehler|BESCHREIBUNG|  
|---------------------|-----------|-----------------|  
|ODBC_ERROR_OUT_OF_MEM|Nicht genügend Arbeitsspeicher.|Das Installationsprogramm konnte die Funktion aufgrund eines fehlenden Speichers nicht ausführen.|  
  
## <a name="comments"></a>Kommentare  
 Diese Funktion wird verwendet, um zu bestimmen, wo der Odbc.ini Eintrag mit DSN-Werten in den Systeminformationen liegt. Wenn *\* pwconfigmode* ODBC_USER_DSN ist, ist der DSN ein Benutzer-DSN, und die Funktion liest aus dem Odbc.ini Eintrag in HKEY_CURRENT_USER. Wenn Sie ODBC_SYSTEM_DSN ist, ist der DSN ein System-DSN, und die Funktion liest aus dem Odbc.ini Eintrag in HKEY_LOCAL_MACHINE. Wenn Sie ODBC_BOTH_DSN, wird HKEY_CURRENT_USER versucht, und wenn Sie fehlschlägt, wird HKEY_LOCAL_MACHINE verwendet.  
  
 Standardmäßig gibt **sqlgetconfigmode** ODBC_BOTH_DSN zurück. Wenn ein Benutzer-DSN oder ein System-DSN durch einen **SQLConfigDataSource**-Befehl erstellt wird, legt die Funktion den Konfigurations Modus auf ODBC_USER_DSN oder ODBC_SYSTEM_DSN fest, um Benutzer-und System-DSNs beim Ändern eines DSN zu unterscheiden. Vor der Rückgabe setzt **SQLConfigDataSource** den Konfigurations Modus auf ODBC_BOTH_DSN zurück.  
  
## <a name="related-functions"></a>Verwandte Funktionen  
  
|Informationen über|Finden Sie unter|  
|---------------------------|---------|  
|Festlegen des Konfigurationsmodus|[Sqlsetconfigmode](../../../odbc/reference/syntax/sqlsetconfigmode-function.md)|
