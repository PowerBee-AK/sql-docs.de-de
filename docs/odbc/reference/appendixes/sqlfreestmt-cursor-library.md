---
description: SQLFreeStmt (Cursorbibliothek)
title: SQLFreeStmt (Cursor Bibliothek) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQLFreeStmt function [ODBC], Cursor Library
ms.assetid: 47bfbd4d-9453-4609-958d-1e05794cb223
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 3b7ebdcfc5a9997efb4301852b1aae3c1408464d
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202819"
---
# <a name="sqlfreestmt-cursor-library"></a>SQLFreeStmt (Cursorbibliothek)
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 In diesem Thema wird die Verwendung der **SQLFreeStmt** -Funktion in der Cursor Bibliothek erläutert. Allgemeine Informationen zu **SQLFreeStmt** finden Sie unter [SQLFreeStmt-Funktion](../../../odbc/reference/syntax/sqlfreestmt-function.md).  
  
 Wenn eine Anwendung **SQLFreeStmt** mit der SQL_UNBIND-Option aufruft, nachdem **SQLExtendedFetch**, **SQLFetch** oder **SQLFetchScroll** aufgerufen wurde, gibt die Cursor Bibliothek einen Fehler zurück. Bevor die Bindung von Resultsetspalten aufgehoben werden kann, muss eine Anwendung **SQLCloseCursor** oder **SQLFreeStmt** mit der SQL_CLOSE-Option aufzurufen.
