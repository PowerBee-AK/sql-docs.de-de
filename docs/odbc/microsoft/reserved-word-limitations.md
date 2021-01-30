---
description: Einschränkungen von reservierten Schlüsselwörtern
title: Einschränkungen für reservierte Wörter | Microsoft-Dokumentation
ms.custom: ''
ms.date: 05/01/2018
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC desktop database drivers [ODBC]
- desktop database drivers [ODBC]
ms.assetid: ed42f083-c9e8-4ee4-9d64-d879bf955c78
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: e615ab4c8222ec7ac679f96f360458dfaab5abb9
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99182575"
---
# <a name="reserved-keyword-limitations"></a>Einschränkungen von reservierten Schlüsselwörtern

Vermeiden Sie die Verwendung von reservierten ODBC-Schlüsselwörtern als Bezeichner in Ihren SQL-Tabellen oder verwandten Objekten. Wenn ein ungerade Fall auftritt, bei dem Sie ein reserviertes Schlüsselwort als Bezeichner verwenden müssen, müssen Sie den Bezeichner mit einem Paar von *Graviszeichen* (') umschließen. Ein weiterer Name für das *Graviszeichen* ist das *Rück Anführungs* Zeichen.

Die Einschränkung des reservierten Schlüssel Worts gilt auch für beliebige Kurzformen der reservierten Schlüsselwörter.

Eine Liste der reservierten ODBC-Schlüsselwörter finden Sie unter:

- [Reservierte ODBC-Schlüsselwörter](../reference/appendixes/reserved-keywords.md).

- Informationen zum *ODBC Programmer es Reference Guide* finden Sie unter [Anhang C: SQL-Grammatik](../reference/appendixes/appendix-c-sql-grammar.md).