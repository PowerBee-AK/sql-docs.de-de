---
description: Cache der Cursorbibliothek
title: Cursor-Bibliotheks Cache | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC cursor library [ODBC], cache
- cursor library [ODBC], cache
- cache [ODBC]
ms.assetid: d6a91cd6-3905-4e3a-98ab-37fce893dbe1
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0de0f04795cd2e0ad8f007155cad2b9329c3d082
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99165371"
---
# <a name="cursor-library-cache"></a>Cache der Cursorbibliothek
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 Für jede Daten Zeile im Resultset werden die Daten für jede gebundene Spalte, die Länge der Daten in den einzelnen gebundenen Spalten und der Status der Zeile von der Cursor Bibliothek zwischengespeichert. Die Cursor Bibliothek verwendet die Werte im Cache, um durch **SQLFetch** und **SQLFetchScroll** zurückzukehren und durchsuchte Anweisungen für positionierte Vorgänge zu erstellen. Weitere Informationen finden Sie unter [Erstellen von durchsuchten Anweisungen](../../../odbc/reference/appendixes/constructing-searched-statements.md).  
  
 In diesem Abschnitt werden die folgenden Themen behandelt:  
  
-   [Spaltendaten](../../../odbc/reference/appendixes/column-data.md)  
  
-   [Länge von Spaltendaten](../../../odbc/reference/appendixes/length-of-column-data.md)  
  
-   [Zeilenstatus](../../../odbc/reference/appendixes/row-status.md)  
  
-   [Speicherort des Caches](../../../odbc/reference/appendixes/location-of-cache.md)
