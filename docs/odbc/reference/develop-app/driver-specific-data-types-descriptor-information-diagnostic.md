---
description: Treiberspezifische Datentypen, Deskriptortypen, Informationstypen, Diagnosetypen und Attribute
title: 'Driver-Specific Typen: Daten, Deskriptor, Informationen, Diagnose | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- driver-specific diagnostic values [ODBC]
- diagnostic information [ODBC], driver-specific values
- ODBC drivers [ODBC], driver-specific diagnostic values
ms.assetid: ad4c76d3-5191-4262-b47c-5dd1d19d1154
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 03cd6b0ed9a424a161f88f4bd525941895d3d201
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100062565"
---
# <a name="driver-specific-data-types-descriptor-types-information-types-diagnostic-types-and-attributes"></a>Treiberspezifische Datentypen, Deskriptortypen, Informationstypen, Diagnosetypen und Attribute
Treiber können Treiber spezifische Werte für Folgendes zuweisen:  
  
-   **SQL-Datentyp Indikatoren** Diese werden in *ParameterType* in **SQLBindParameter** und in *DataType* in **SQLGetTypeInfo** verwendet und von **SQLColAttribute**, **SQLColumns**, **SQLDescribeCol**, **SQLGetTypeInfo**, **SQLDescribeParam**, **sqlprocedurecolrens** und **SQLSpecialColumns** zurückgegeben.  
  
-   **Deskriptorfelder** Diese werden in " *fieldidentifier* " in **SQLColAttribute**, **SQLGetDescField** und **SQLSetDescField** verwendet.  
  
-   **Diagnose Felder** Diese werden in *DiagIdentifier* in **SQLGetDiagField** und **SQLGetDiagRec** verwendet.  
  
-   **Informationstypen** Diese werden in *InfoType* in **SQLGetInfo** verwendet.  
  
-   **Verbindungs-und Anweisungs Attribute** Diese werden im- *Attribut* in **SQLGetConnectAttr**, **SQLGetStmtAttr**, **SQLSetConnectAttr** und **SQLSetStmtAttr** verwendet.  
  
 Für jedes dieser Elemente gibt es zwei Sätze von Werten: Werte, die für die Verwendung durch ODBC reserviert sind, und Werte, die für die Verwendung durch Treiber reserviert sind. Vor der Implementierung von treiberspezifischen Werten muss ein treiberwriter einen Wert für die einzelnen treiberspezifischen Typen, Felder oder Attribute der geöffneten Gruppe anfordern. Verwenden Sie für die Entwicklung neuer Treiber den in der folgenden Tabelle beschriebenen Bereich. Der Treiber-Manager von ODBC 3,8 generiert keinen Fehler, wenn ein unbekannter Wert verwendet wird, der nicht im unten beschriebenen Bereich liegt. Spätere Versionen des Treiber-Managers generieren jedoch möglicherweise einen Fehler, wenn unbekannte Werte empfangen werden, die nicht im Bereich liegen.  
  
 Wenn einer dieser Werte an eine ODBC-Funktion übermittelt wird, muss der Treiber überprüfen, ob der Wert gültig ist. Treiber geben SQLSTATE HYC00 (optionales Feature nicht implementiert) für Treiber spezifische Werte zurück, die für andere Treiber gelten.  
  
 Ab ODBC 3,8 können treiberwriter Treiber spezifische Attribute innerhalb eines reservierten Bereichs zuordnen.  
  
> [!NOTE]  
>  Der ODBC 3,8-Treiber-Manager überprüft weder diese Bereiche noch für die Abwärtskompatibilität. Eine zukünftige Version des Treiber-Managers kann Sie jedoch erzwingen.  
  
|Attributtyp|ODBC-Datentyp|Treiber spezifische Bereichs Basis|Treiber spezifisches Bereichs Limit|ODBC-Konstante für Treiber spezifische Wertebereichs Basis|  
|--------------------|--------------------|---------------------------------|----------------------------------|---------------------------------------------------------|  
|SQL-Datentyp Indikatoren|SQLSMALLINT|0x4000|0x7FFF|SQL_DRIVER_SQL_TYPE_BASE|  
|Deskriptorfelder|SQLSMALLINT|0x4000|0x7FFF|SQL_DRIVER_DESCRIPTOR_BASE|  
|Diagnose Felder|SQLSMALLINT|0x4000|0x7FFF|SQL_DRIVER_DIAGNOSTIC_BASE|  
|Informationstypen|Sqlusmallint|0x4000|0x7FFF|SQL_DRIVER_INFO_TYPE_BASE|  
|Verbindungs Attribute|SQLINTEGER|0x00004000|0x00007fff|SQL_DRIVER_CONNECT_ATTR_BASE|  
|Anweisungs Attribute|SQLINTEGER|0x00004000|0x00007fff|SQL_DRIVER_STATEMENT_ATTR_BASE|  
  
> [!NOTE]  
>  Treiber spezifische Datentypen, Deskriptorfelder, Diagnose Felder, Informationstypen, Anweisungs Attribute und Verbindungs Attribute müssen in der Treiber Dokumentation beschrieben werden. Wenn einer dieser Werte an eine ODBC-Funktion übermittelt wird, muss der Treiber überprüfen, ob der Wert gültig ist. Treiber geben SQLSTATE HYC00 (optionales Feature nicht implementiert) für Treiber spezifische Werte zurück, die für andere Treiber gelten.  
  
 Die Basiswerte werden definiert, um die Treiberentwicklung zu vereinfachen. Treiber spezifische Diagnose Attribute können z. b. im folgenden Format definiert werden:  
  
```  
SQL_DRIVER_DIAGNOSTIC_BASE+0, SQL_DRIVER_DIAGNOSTIC_BASE +1  
```
