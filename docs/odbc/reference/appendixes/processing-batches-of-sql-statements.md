---
description: Verarbeiten von Batches von SQL-Anweisungen
title: Verarbeiten von Batches von SQL-Anweisungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC cursor library [ODBC], batches
- ODBC cursor library [ODBC], statement processing
- cursor library [ODBC], batches
- SQL statements [ODBC], cursor library
- cursor library [ODBC], statement processing
- SQL statements [ODBC], batches
- batches [ODBC], processing batches of SQL statements
ms.assetid: 04b93ef9-11de-47a3-8bd8-ba963c42f182
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d2c70dc742b170f608246eff1bbb12234a26414b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99209489"
---
# <a name="processing-batches-of-sql-statements"></a>Verarbeiten von Batches von SQL-Anweisungen
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 Die Cursor Bibliothek unterstützt keine Batches von SQL-Anweisungen, einschließlich der SQL-Anweisungen, für die das Attribut der SQL_ATTR_PARAMSET_SIZE Anweisung größer als 1 ist. Wenn eine Anwendung einen Batch von SQL-Anweisungen an die Cursor Bibliothek übermittelt, sind die Ergebnisse nicht definiert.
