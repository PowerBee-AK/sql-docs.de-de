---
description: Skalarfunktion-Escapesequenz
title: Escapesequenz für Skalarfunktionen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- escape sequences [ODBC], scalar function
- scalar functions [ODBC], escape sequences
- ODBC escape sequences [ODBC], scalar function
ms.assetid: aaf5d516-e090-445f-8839-9e39581c69c7
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f17323281ba666d9657b8c1f7e555b61ef24e19f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187123"
---
# <a name="scalar-function-escape-sequence"></a>Skalarfunktion-Escapesequenz
ODBC verwendet Escapesequenzen für Skalarfunktionen. Die Syntax dieser Escapesequenz lautet wie folgt:  
  
```  
{fn scalar-function}  
```  
  
## <a name="remarks"></a>Bemerkungen  
 In der BNF-Notation lautet die Syntax wie folgt:  
  
 *ODBC-Scalar-Function-Escape* :: =  
  
 *ODBC-ESC-Initiator* FN *Scalar-Funktion ODBC-ESC-Terminator*  
  
 *Skalarfunktion* :: = *Funktionsname* (*Argument-List*)  
  
 (Die Definitionen für den nicht terminale *-Funktionsnamen* und den *Funktionsnamen* (*Argument-List*) werden aus der Liste der Skalarfunktionen in [Anhang E: skalare Funktionen](../../../odbc/reference/appendixes/appendix-e-scalar-functions.md)abgeleitet.)  
  
 *ODBC-ESC-Initiator* :: = {  
  
 *ODBC-ESC-Terminator* :: =}  
  
 Um zu ermitteln, ob die Datenquelle Prozeduren unterstützt und der Treiber die ODBC-Prozedur Aufruf Syntax unterstützt, kann eine Anwendung **SQLGetInfo** aufrufen. Weitere Informationen finden Sie unter [Anhang E: Skalarfunktionen](../../../odbc/reference/appendixes/appendix-e-scalar-functions.md).
