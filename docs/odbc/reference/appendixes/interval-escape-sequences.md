---
description: Intervall-Escapesequenzen
title: Intervall-Escapesequenzen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- interval literals [ODBC]
- escape sequences [ODBC], interval
- ODBC escape sequences [ODBC], interval
ms.assetid: 303e8dab-8f13-4fa5-857f-15cc1f75bdd6
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0badac832ee4cf4e29f148dbd39a7989536b9c29
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99176499"
---
# <a name="interval-escape-sequences"></a>Intervall-Escapesequenzen
ODBC verwendet Escapesequenzen für intervallliterale. Die Syntax dieser Escapesequenz lautet wie folgt:  
  
 {*Interval-Literale*}  
  
 Die BNF-Syntax von *Interval-literalen* finden Sie im Abschnitt [Intervall Literalsyntax](../../../odbc/reference/appendixes/interval-literal-syntax.md) weiter unten in diesem Anhang.  
  
 Die Literale Escapesequenz für Intervalle wird unterstützt, wenn die Intervall Datentypen von der Datenquelle unterstützt werden. Eine Anwendung sollte **SQLGetTypeInfo** aufrufen, um zu bestimmen, ob diese Datentypen unterstützt werden.
