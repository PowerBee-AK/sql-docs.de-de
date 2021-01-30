---
description: Visual FoxPro-Felddatentypen
title: Visual FoxPro-Feld Datentypen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- field data types [ODBC]
- Visual FoxPro ODBC driver [ODBC], data types
ms.assetid: 50b733dc-679a-4b10-bc5d-98bb474dead2
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 2032ee25039364186f33486e4662b84c36c06947
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99207476"
---
# <a name="visual-foxpro-field-data-types"></a>Visual FoxPro-Felddatentypen
In der folgenden Tabelle sind die Werte für das *FieldType* -Argument in ALTER TABLE und CREATE TABLE aufgeführt. Außerdem wird angegeben, ob *nfieldwidth* -und *nprecision* -Argumente erforderlich sind.  
  
|*FieldType*|*Nfieldwidth*|*ngenauigkeit*|BESCHREIBUNG|  
|-----------------|-------------------|------------------|-----------------|  
|B|-|T|Double|  
|C|N|-|Zeichenfeld der Breite *n*|  
|D|-|-|Date|  
|F|N|T|Gleitendes numerisches Feld der Breite *n* mit *d* Dezimalstellen|  
|G|-|-|Allgemein|  
|I|-|-|Integer|  
|L|-|-|Logisch|  
|M|-|-|Memo|  
|N|N|T|Numerisches Feld der Breite *n* mit *d* Dezimalstellen|  
|T|-|-|Datetime|  
|J|-|-|Währung|
