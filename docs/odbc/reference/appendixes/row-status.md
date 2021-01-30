---
description: Zeilenstatus
title: Zeilen Status | Microsoft-Dokumentation
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
- row status [ODBC]
- cache [ODBC]
ms.assetid: 0f0b1fb6-f697-4ced-811c-2908e210bc71
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 491e0b420e31f1fe8e66c73f9ab8d89cb1e7e1cd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187156"
---
# <a name="row-status"></a>Zeilenstatus
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 Die Cursor Bibliothek erstellt einen Puffer im Cache für den Zeilen Status. Die Cursor Bibliothek Ruft Werte für das Zeilen Status Array (angegeben mit dem SQL_ATTR_ROW_STATUS_PTR-Anweisungs Attribut) aus diesem Puffer ab. Die Cursor Bibliothek legt den Puffer für jede Zeile auf Folgendes fest:  
  
-   SQL_ROW_DELETED, wenn eine positionierte DELETE-Anweisung in der Zeile ausgeführt wird.  
  
-   SQL_ROW_ERROR, wenn beim Abrufen der Zeile aus der Datenquelle mit **SQLFetch** ein Fehler auftritt.  
  
-   SQL_ROW_SUCCESS, wenn die Zeile mit **SQLFetch** erfolgreich aus der Datenquelle abgerufen wurde.  
  
-   SQL_ROW_UPDATED, wenn eine positionierte UPDATE-Anweisung in der Zeile ausgeführt wird.
