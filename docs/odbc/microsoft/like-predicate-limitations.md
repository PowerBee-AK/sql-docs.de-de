---
description: Einschränkungen des LIKE-Prädikats
title: LIKE-Prädikat Einschränkungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- LIKE predicate limitations [ODBC]
- ODBC SQL grammar, LIKE predicate limitations
ms.assetid: dbd39099-caf6-4c4c-9ad8-f6c63c1bd5e4
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 4925ff83d8dafc1cce7c0a58a17685fcf30371f6
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199898"
---
# <a name="like-predicate-limitations"></a>Einschränkungen des LIKE-Prädikats
Wenn die Daten in einer Spalte mehr als 255 Zeichen enthalten, basiert der Like-Vergleich nur auf den ersten 255 Zeichen.  
  
 Ein like, der in einer Prozedur verwendet wird, wird nur mit Konstanten Mustern unterstützt. Die Desktop-Datenbanktreiber unterstützen SQL-92 wie Musterabgleich.  
  
 Die Verwendung einer Escape-Klausel in einem LIKE-Prädikat wird nicht unterstützt.  
  
 Ein Like-Vergleich sollte nicht für eine Spalte mit Daten eines numerischen Datentyps oder eines float-Datentyps ausgeführt werden. Die Ergebnisse sind möglicherweise nicht vorhersehbar. Weitere Informationen finden Sie im *Microsoft Jet Datenbank-Engine Programmer es Guide*.
