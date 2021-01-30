---
description: Einschränkungen der CONVERT-Funktion
title: Einschränkungen für die Konvertierung von Funktionen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC SQL grammar, CONVERT function limitations
- Convert function limitations [ODBC]
ms.assetid: 3c81fc58-57f0-4dd7-be16-2b146eb15cbc
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d7f953f272b30095e31e68fa1bc2b6972bb4b6d3
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99159549"
---
# <a name="convert-function-limitations"></a>Einschränkungen der CONVERT-Funktion
Typkonvertierungs Fehler führen dazu, dass die betroffene Spalte auf NULL festgelegt wird.  
  
 Weder der Date-noch der timestamp-Datentyp kann von der Convert-Funktion in einen anderen Datentyp (oder selbst) konvertiert werden.
