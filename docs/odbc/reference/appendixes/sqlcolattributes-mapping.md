---
description: SQLColAttributes-Zuordnung
title: SQLColAttribute-Zuordnung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- mapping deprecated functions [ODBC], SQLColAttributes
- SQLColAttribute function [ODBC], mapping
ms.assetid: 30e25719-176b-4c48-97d4-920766b22412
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 7c8ff9d861663e1bb9e52ad5e083fa4fed809139
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202893"
---
# <a name="sqlcolattributes-mapping"></a>SQLColAttributes-Zuordnung
Wenn eine Anwendung **SQLColAttribute** über einen ODBC *3. x* -Treiber aufruft, wird der Aufruf von **SQLColAttribute** wie folgt **SQLColAttribute** zugeordnet:  
  
> [!NOTE]
>  Das Präfix, das in den *fieldidentifier* -Werten in ODBC *3. x* verwendet wurde, wurde von dem in ODBC *2. x* verwendeten Wert geändert. Das neue Präfix ist "SQL_DESC"; das alte Präfix war "SQL_COLUMN".  
  
1.  Wenn es sich bei der Anwendung um eine ODBC *2. x* -Anwendung handelt, ist der Typ " *Typ* " SQL_COLUMN_TYPE, und der zurückgegebene Typ ist ein präziser DateTime-Typ. der Treiber-Manager ordnet die Rückgabewerte für Datums-, Uhrzeit-und Zeitstempel Codes zu.  
  
2.  Wenn *fdesctype* SQL_COLUMN_NAME, SQL_COLUMN_NULLABLE oder SQL_COLUMN_COUNT ist, ruft der Treiber-Manager **SQLColAttribute** im Treiber auf, wobei das *fieldidentifier* -Argument entsprechend SQL_DESC_NAME, SQL_DESC_NULLABLE oder SQL_DESC_COUNT zugeordnet ist *.* Alle anderen Werte von *fdesctype* werden an den Treiber übermittelt.  
  
 Ein ODBC *3. x* -Treiber muss alle ODBC *3. x* - *fieldidentifier* unterstützen, die für **SQLColAttribute** aufgeführt sind.  
  
 Ein ODBC *3. x* -Treiber muss SQL_COLUMN_PRECISION und SQL_DESC_PRECISION, SQL_COLUMN_SCALE und SQL_DESC_SCALE sowie SQL_COLUMN_LENGTH und SQL_DESC_LENGTH unterstützen. Diese Werte unterscheiden sich, da Genauigkeit, Dezimalstellen und Länge in ODBC *3. x* anders definiert sind als in ODBC *2. x*. Weitere Informationen finden Sie unter [Spaltengröße, Dezimalstellen, Oktettlänge übertragen und Anzeige Größe](../../../odbc/reference/appendixes/column-size-decimal-digits-transfer-octet-length-and-display-size.md) in Anhang D: Datentypen.
