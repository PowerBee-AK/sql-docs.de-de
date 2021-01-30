---
description: SQL_ARD_TYPE
title: SQL_ARD_TYPE | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- data types [ODBC], pseudo-type identifiers
- pseudo-type identifiers [ODBC], SQL_ARD_TYPE
- SQL_ARD_TYPE [ODBC]
ms.assetid: 8d87ca10-f955-4284-8689-e9f4cc31e7ae
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 43d8ce804fc66fd8d9a305868cf1a8b22cf8ff7d
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187072"
---
# <a name="sql_ard_type"></a>SQL_ARD_TYPE
Der SQL_ARD_TYPE-Typbezeichner wird verwendet, um anzugeben, dass die Daten in einem Puffer vom Typ sind, der im SQL_DESC_CONCISE_TYPE-Feld der ARD angegeben wird. SQL_ARD_TYPE wird im *TargetType* -Argument eines Aufrufens von **SQLGetData** anstelle eines bestimmten Datentyps eingegeben und ermöglicht einer Anwendung, den Datentyp des Puffers zu ändern, indem das Deskriptorfeld geändert wird. Dieser Wert bindet den Datentyp des *\* targetvalueptr* -Puffers an das Deskriptorfeld. (SQL_ARD_TYPE wird nicht in einen Aufruf von **SQLBindCol** oder **SQLBindParameter** eingegeben, da der Typ des gebundenen Puffers bereits an die Felder SQL_DESC_TYPE und SQL_DESC_CONCISE_TYPE gebunden ist und jederzeit durch Ändern eines dieser Felder geändert werden kann.)  
  
 Der SQL_ARD_TYPE-Typbezeichner kann verwendet werden, um nicht standardmäßige Werte für die führende Genauigkeit und Sekunden Genauigkeit von Intervall Datentypen sowie Genauigkeits-und Skalierungs Werte für den SQL_C_NUMERIC Datentyp anzugeben. Weitere Informationen finden Sie weiter unten in diesem Anhang unter Überschreiben der [Standardgenauigkeit und der Genauigkeit von Sekunden für Intervall Datentypen](../../../odbc/reference/appendixes/overriding-default-leading-and-seconds-precision-for-interval-data-types.md) und Überschreiben der [Standardgenauigkeit und-Dezimalstelle für numerische Datentypen](../../../odbc/reference/appendixes/overriding-default-precision-and-scale-for-numeric-data-types.md).
