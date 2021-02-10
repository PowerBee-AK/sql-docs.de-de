---
description: Grundlegendes zu Cursorn und Sperren
title: Grundlegendes zu Cursorn | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- locks [ADO]
- cursors [ADO]
ms.assetid: c1b7d7e6-1707-4ce2-863f-0c6dea967df6
author: rothja
ms.author: jroth
ms.openlocfilehash: 088e692df37cab549a01b3cbe0bf869ebaf24f1a
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100032332"
---
# <a name="understanding-cursors-and-locks"></a>Grundlegendes zu Cursorn und Sperren
Es ist wichtig, die Funktionsweise von Cursorn zu verstehen, sodass Sie den besten und effizientesten Cursortyp für die Datenzugriffs Anforderungen einer Anwendung auswählen können. Eine weniger optimale Cursor Konfiguration kann dazu führen, dass Datenzugriffs Vorgänge sehr langsam sind.  
  
 Viele Funktionen des ADO- **Recordset** -Objekts werden durch den Typ und die Position des Cursors sowie durch den Sperrentyp bestimmt.  
  
 In diesem Abschnitt werden die folgenden Themen behandelt:  
  
-   [Was ist ein Cursor?](../../../ado/guide/data/what-is-a-cursor.md)  
  
-   [Cursor Typen](../../../ado/guide/data/types-of-cursors-ado.md)  
  
-   [Die Bedeutung der Cursorposition](../../../ado/guide/data/the-significance-of-cursor-location.md)  
  
-   [Microsoft Cursor-Dienst für OLE DB](../../../ado/guide/data/the-microsoft-cursor-service-for-ole-db.md)  
  
-   [Was ist eine Sperre?](../../../ado/guide/data/what-is-a-lock.md)  
  
-   [Verwenden von CacheSize](../../../ado/guide/data/using-cachesize.md)  
  
-   [Cursor und Merkmale der Sperre](../../../ado/guide/data/cursor-and-lock-characteristics.md)
