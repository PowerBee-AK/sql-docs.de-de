---
description: SQLGetFunctions (Cursorbibliothek)
title: SQLGetFunctions (Cursor Bibliothek) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQLGetFunctions function [ODBC], Cursor Library
ms.assetid: 931acd12-4eb6-4a78-9a77-157a18a9a2d0
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 9414aa4d2be551ab3b6a44193f6b6c17e2deb145
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202755"
---
# <a name="sqlgetfunctions-cursor-library"></a>SQLGetFunctions (Cursorbibliothek)
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 In diesem Thema wird die Verwendung der **SQLGetFunctions** -Funktion in der Cursor Bibliothek erläutert. Allgemeine Informationen zu **SQLGetFunctions** finden Sie unter [SQLGetFunctions-Funktion](../../../odbc/reference/syntax/sqlgetfunctions-function.md).  
  
 Wenn Sie **SQLGetFunctions** aufrufen, gibt die Cursor Bibliothek zusätzlich zu den vom Treiber unterstützten Funktionen zurück, dass **SQLExtendedFetch**, **SQLFetchScroll**, **SQLSetPos** und **SQLSetScrollOptions** unterstützt werden.
