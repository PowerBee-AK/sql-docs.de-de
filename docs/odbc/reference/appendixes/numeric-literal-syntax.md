---
description: Syntax von numerischen Literalen
title: Numerische Literale Syntax | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC literals [ODBC], numeric
- numeric literals [ODBC]
- literals [ODBC], numeric
ms.assetid: fb17498d-4f1d-4b3d-b33d-1e62c7d3c32d
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 541f2fa53d6aeb9a387117b17f0917cb110dc630
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99193296"
---
# <a name="numeric-literal-syntax"></a>Syntax von numerischen Literalen
Die folgende Syntax wird für numerische Literale in ODBC verwendet:  
  
 *numeric-Literale* :: = *Signed-numeric-Literal &#124; nicht signiertes numeric-Literale*  
  
 *Signed-numeric-Literale* :: = [*Sign*] *unsigned-numeric-Literale*  
  
 *unsigned-numeric-Literale* :: = *Exact-numeric-Literal&#124; ungefähre numerische Literale*  
  
 *Exact-numeric-Literale* :: = *unsigned-Integer* [*Period*[*unsigned-Integer*]] *&#124;period unsigned-Integer*  
  
 *Sign* :: = *plus-Sign &#124; minus-Sign*  
  
 *ungefähre-numeric-Literale* :: = *Mantisse E Exponent*  
  
 *Mantisse* :: = *Exact-numeric-Literale*  
  
 *Exponent* :: = *-Ganzzahl* mit Vorzeichen  
  
 *signed-integer* :: = [*Sign*] *nicht signierte Ganzzahl*  
  
 *unsigned-Integer* :: = *Digit...*  
  
 *Plus-sign* :: = *+*  
  
 *Minuszeichen* :: =-  
  
 *Ziffer* :: = 1 &#124; 2 &#124; 3 &#124; 4 &#124; 5 &#124; 6 &#124; 7 &#124; 8 &#124; 9 &#124; 0  
  
 *Period* :: =.
