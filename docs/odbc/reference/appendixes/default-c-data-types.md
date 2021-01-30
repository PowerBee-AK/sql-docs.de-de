---
description: Standardmäßige C-Datentypen
title: C-Standard Datentypen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- data types [ODBC], pseudo-type identifiers
- pseudo-type identifiers [ODBC], about pseudo-type identifiers
- pseudo-type identifiers [ODBC]
ms.assetid: 229140ae-af8f-4ec8-9ccf-1e92360e0bac
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: fd7f50e58fd84cec5938aacc598d12e6d733fcdc
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99194894"
---
# <a name="default-c-data-types"></a>Standardmäßige C-Datentypen
Wenn eine Anwendung SQL_C_DEFAULT in **SQLBindCol**, **SQLGetData** oder **SQLBindParameter** angibt, geht der Treiber davon aus, dass der C-Datentyp der Ausgabe oder des Eingabe Puffers dem SQL-Datentyp der Spalte oder des Parameters entspricht, an die der Puffer gebunden ist.  
  
> [!IMPORTANT]  
>  Interoperable Anwendungen sollten SQL_C_DEFAULT nicht verwenden. Stattdessen sollten Sie immer den C-Typ des Puffers angeben, den Sie verwenden. Dies liegt daran, dass Treiber den Standard-C-Typ aus den folgenden Gründen nicht immer ordnungsgemäß bestimmen können:  
  
-   Wenn das DBMS einen SQL-Datentyp einer Spalte oder eines Parameters herauf stuft, kann der Treiber den ursprünglichen SQL-Datentyp einer Spalte oder eines Parameters nicht ermitteln. Daher kann der entsprechende C-Standard Datentyp nicht bestimmt werden.  
  
-   Wenn der Treiber nicht bestimmen kann, ob eine bestimmte Spalte oder ein bestimmter Parameter signiert ist, wie es häufig der Fall ist, wenn er vom DBMS verarbeitet wird, kann der Treiber nicht ermitteln, ob der entsprechende C-Standard Datentyp signiert oder nicht signiert werden soll.  
  
     Da SQL_C_DEFAULT nur als Programmier Zweck bereitgestellt wird, verliert die Anwendung keine Funktionalität, wenn Sie den tatsächlichen C-Datentyp angibt.  
  
 Eine Tabelle, die den c-Standard Datentyp für jeden SQL-Datentyp enthält, ist in den Daten [Typen "Daten aus SQL in C" weiter](../../../odbc/reference/appendixes/converting-data-from-sql-to-c-data-types.md)unten in diesem Anhang enthalten.
