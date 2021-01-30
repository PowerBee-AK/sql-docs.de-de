---
description: Verwenden von Datentypbezeichnern
title: Verwenden von Datentyp bezeichgern | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- data types [ODBC], identifiers
- identifiers [ODBC], data types
ms.assetid: 467e0c0c-a818-4737-8a24-3d8e15c7e162
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: cd38f5ddb62a28bc3ec2658dca621769e13ab481
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202435"
---
# <a name="using-data-type-identifiers"></a>Verwenden von Datentypbezeichnern
Anwendungen verwenden Datentyp Bezeichner auf zwei Arten: zum Beschreiben der Puffer für den Treiber und zum Abrufen von Metadaten über das Resultset vom Treiber, damit Sie bestimmen können, welche Art von C-Puffer zum Speichern der Daten verwendet werden sollen. Anwendungen nennen die folgenden Funktionen, um diese Aufgaben auszuführen:  
  
-   **SQLBindParameter**, **SQLBindCol** und **SQLGetData** , um den C-Datentyp von Anwendungs Puffern zu beschreiben.  
  
-   **SQLBindParameter** : Beschreibt den SQL-Datentyp dynamischer Parameter.  
  
-   **SQLColAttribute** und **SQLDescribeCol** : um die SQL-Datentypen von Resultsetspalten abzurufen.  
  
-   **Sqldescribeparameter** -zum Abrufen der SQL-Datentypen von Parametern.  
  
-   **SQLColumns**, **sqlprocedurecolumschlag** und **SQLSpecialColumns** : um die SQL-Datentypen verschiedener Schema Informationen abzurufen  
  
-   **SQLGetTypeInfo** -zum Abrufen einer Liste unterstützter Datentypen  
  
 Datentyp Bezeichner werden im SQL_DESC_CONCISE_TYPE-Feld eines Deskriptors gespeichert. Die deskriptorfunktionen **SQLSetDescField** und **SQLSetDescRec** können mit den entsprechenden Typen verwendet werden, um die in der vorherigen Liste aufgeführten Aufgaben auszuführen. Weitere Informationen finden Sie unter [SQLSetDescField](../../../odbc/reference/syntax/sqlsetdescfield-function.md).
