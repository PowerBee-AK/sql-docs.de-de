---
description: Einschränkungen des gregorianischen Kalenders
title: Einschränkungen des gregorianischen Kalenders | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- data types [ODBC], Gregorian calendar
- Gregorian calendar [ODBC]
ms.assetid: 70667410-c582-4369-8e06-9d98e21cd2bf
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: dbab6e1ef26843807c67e3d3daba9a66e054d8f1
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99165409"
---
# <a name="constraints-of-the-gregorian-calendar"></a>Einschränkungen des gregorianischen Kalenders
Die Datums-und datetime-Datentypen und die nachfolgenden Felder der Intervall Datentypen müssen den Einschränkungen des gregorianischen Kalenders entsprechen. Diese Einschränkungen lauten wie folgt:  
  
-   Der Wert des Monats Felds muss zwischen 1 und 12 (einschließlich) liegen.  
  
-   Der Wert des Tages Felds muss zwischen 1 und der Anzahl der Tage im Monat liegen. Die Anzahl der Tage im Monat wird von den Werten der Felder Jahr und Monat bestimmt und kann 28, 29, 30 oder 31 sein. (Die Anzahl der Tage im Monat kann auch davon abhängen, ob es sich um ein Schaltjahr handelt.)  
  
-   Der Wert des Felds "Hour" muss zwischen 0 und 23 (einschließlich) liegen.  
  
-   Der Wert des Felds Minute muss zwischen 0 und 59 (einschließlich) liegen.  
  
-   Im Feld "nachfolgende Sekunden" der Intervall Datentypen muss der Wert des Felds "seconds" zwischen 0 und 59,9 (*n*) (einschließlich) liegen, wobei *n* die Anzahl der Ziffern in der Genauigkeit der Sekundenbruchteile ist.  
  
-   Im Feld "nachfolgende Sekunden" der DateTime-Datentypen muss der Wert des Felds "seconds" zwischen 0 und 61,9 (*n*) (einschließlich) liegen, wobei *n* die Anzahl von 9 Ziffern angibt und der Wert von *n* die Genauigkeit der Sekundenbruchteile ist. (Der Bereich von Sekunden lässt bis zu zwei Schaltsekunden zu, um die Synchronisierung der zeitgleich zeitig beizubehalten.)
