---
description: Verarbeiten von SQL-Anweisungen
title: Verarbeiten von SQL-Anweisungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC cursor library [ODBC], statement processing
- SQL statements [ODBC], cursor library
- cursor library [ODBC], statement processing
ms.assetid: 54dad6a3-e86c-477b-ba7c-4e95e0385ec1
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: ed0e9bddba0b23d17e6e880e2b83af2bff359fe9
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99199876"
---
# <a name="processing-sql-statements"></a>Verarbeiten von SQL-Anweisungen
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 Die ODBC-Cursor Bibliothek übergibt alle SQL-Anweisungen direkt an den Treiber, mit Ausnahme der folgenden:  
  
-   Positionierte UPDATE-und DELETE-Anweisungen  
  
-   **Select for Update** -Anweisungen  
  
-   SQL-Anweisungen im Batch Modus  
  
 Um positionierte UPDATE-und DELETE-Anweisungen auszuführen und den Cursor in einer Zeile zum Aufrufen von **SQLGetData** für diese Zeile zu positionieren, erstellt die Cursor Bibliothek eine gesuchte Anweisung, die die Zeile identifiziert.  
  
 In diesem Abschnitt werden die folgenden Themen behandelt:  
  
-   [Verarbeiten von positionierten UPDATE- und DELETE-Anweisungen](../../../odbc/reference/appendixes/processing-positioned-update-and-delete-statements.md)  
  
-   [Verarbeiten von SELECT FOR UPDATE-Anweisungen](../../../odbc/reference/appendixes/processing-select-for-update-statements.md)  
  
-   [Verarbeiten von Batches von SQL-Anweisungen](../../../odbc/reference/appendixes/processing-batches-of-sql-statements.md)  
  
-   [Erstellen von searched-Anweisungen](../../../odbc/reference/appendixes/constructing-searched-statements.md)
