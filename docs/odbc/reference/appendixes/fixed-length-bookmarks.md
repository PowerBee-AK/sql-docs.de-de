---
description: Textmarke mit fester Länge
title: Fixed-Length Lesezeichen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- backward compatibility [ODBC], bookmarks
- bookmarks [ODBC]
- compatibility [ODBC], bookmarks
- fixed-length bookmarks [ODBC]
ms.assetid: cbd8185e-fb03-408f-b80b-1a2e164534fd
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 2d5eb7acd97a83be0d150cec8b19a5a3e25a7bf6
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99194806"
---
# <a name="fixed-length-bookmarks"></a>Textmarke mit fester Länge
Wenn ein ODBC *3. x* -Treiber mit einer ODBC *2. x* -Anwendung verwendet werden soll, die Lesezeichen mit fester Länge verwendet, muss der Treiber Folgendes unterstützen:  
  
-   SQL_UB_ON als Wert für die Option SQL_USE_BOOKMARKS Anweisung aus. (SQL_UB_ON in ODBC *3. x* als veraltet markiert.)  
  
-   Die SQL_GET_BOOKMARK Anweisungs Option.
