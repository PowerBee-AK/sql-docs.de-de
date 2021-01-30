---
description: SQLRowCount (Cursorbibliothek)
title: SQLRowCount (Cursor Bibliothek) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQLRowCount function [ODBC], Cursor Library
ms.assetid: 781cf5a5-325e-4523-8633-d96d9e98277c
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 9a8efc6fdef2a3bef563a5289acdef55958a03be
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202680"
---
# <a name="sqlrowcount-cursor-library"></a>SQLRowCount (Cursorbibliothek)
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 In diesem Thema wird die Verwendung der **SQLRowCount** -Funktion in der Cursor Bibliothek erläutert. Allgemeine Informationen zu **SQLRowCount** finden Sie unter [SQLRowCount-Funktion](../../../odbc/reference/syntax/sqlrowcount-function.md).  
  
 Wenn eine Anwendung **SQLRowCount** mit der dem Cursor zugeordneten Anweisung aufruft, gibt die Cursor Bibliothek die Anzahl der Daten Zeilen zurück, die Sie vom Treiber abgerufen hat.  
  
 Wenn eine Anwendung **SQLRowCount** mit der-Anweisung aufruft, die einer positionierten Update-oder DELETE-Anweisung zugeordnet ist, gibt die Cursor Bibliothek die Anzahl der von der Anweisung betroffenen Zeilen zurück.  
  
 Wenn eine Anwendung **SQLRowCount** nach einer **Select** -Anweisung aufruft, gibt die Cursor Bibliothek-1 zurück.
