---
description: SQLGetInfo (Cursorbibliothek)
title: SQLGetInfo (Cursor Bibliothek) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQLGetInfo function [ODBC], Cursor Library
ms.assetid: 1b4d220d-2c07-4f56-987e-36813bb1a6ce
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 9fc11d16d145a37db4fdc50ad7f9907532fe747c
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202768"
---
# <a name="sqlgetinfo-cursor-library"></a>SQLGetInfo (Cursorbibliothek)
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 In diesem Thema wird die Verwendung der **SQLGetInfo** -Funktion in der Cursor Bibliothek erläutert. Allgemeine Informationen zu **SQLGetInfo** finden Sie unter [SQLGetInfo-Funktion](../../../odbc/reference/syntax/sqlgetinfo-function.md).  
  
 Die Cursor Bibliothek gibt Werte für die folgenden Werte von *InfoType* zurück (&#124; stellt ein bitweises OR dar); für alle anderen Werte von *InfoType* wird **SQLGetInfo** im Treiber aufgerufen.  
  
|*Infotype*|Rückgabewert|  
|----------------|--------------------|  
|SQL_BOOKMARK_PERSISTENCE|SQL_BP_SCROLL|  
|SQL_DYNAMIC_CURSOR_ATTRIBUTES1|0|  
|SQL_DYNAMIC_CURSOR_ATTRIBUTES2|0|  
|SQL_FETCH_DIRECTION [1]|SQL_FD_FETCH_ABSOLUTE &#124; SQL_FD_FETCH_FIRST &#124; SQL_FD_FETCH_LAST &#124; SQL_FD_FETCH_NEXT &#124; SQL_FD_FETCH_PRIOR &#124; SQL_FD_FETCH_RELATIVE &#124; SQL_FD_FETCH_BOOKMARK|  
|SQL_FORWARD_ONLY_CURSOR_ATTRIBUTES1|SQL_CA1_NEXT &#124; SQL_CA1_ABSOLUTE &#124; SQL_CA1_RELATIVE &#124; SQL_CA1_LOCK_NO_CHANGE &#124; SQL_CA1_POS_POSITION &#124; SQL_CA1_POSITIONED_DELETE &#124; SQL_CA1_POSITIONED_UPDATE &#124; SQL_CA1_SELECT_FOR_UPDATE|  
|SQL_FORWARD_ONLY_CURSOR_ATTRIBUTES2|SQL_CA2_READ_ONLY_CONCUR &#124; SQL_CA2_OPT_VALUES_CONCURRENCY &#124; SQL_CA2_SENSITIVITY_UPDATES|  
|SQL_GETDATA_EXTENSIONS|SQL_GD_BLOCK &#124; alle Werte zurück, die vom Treiber Hinweis zurückgegeben werden **:**  wenn Daten mit **SQLFetchScroll** abgerufen werden, unterstützt **SQLGetData** die Funktionen, die mit dem SQL_GD_ANY_COLUMN und SQL_GD_BOUND Bitmasks angegeben werden.|  
|SQL_KEYSET_DRIVEN_CURSOR_ATTRIBUTES1|0|  
|SQL_KEYSET_DRIVEN_CURSOR_ATTRIBUTES2|0|  
|SQL_LOCK_TYPES [1]|SQL_LCK_NO_CHANGE|  
|SQL_STATIC_CURSOR_ATTRIBUTES1|SQL_CA1_NEXT &#124; SQL_CA1_ABSOLUTE &#124; SQL_CA1_RELATIVE &#124; SQL_CA1_BOOKMARK &#124; SQL_CA1_LOCK_NO_CHANGE &#124; SQL_CA1_POS_POSITION &#124; SQL_CA1_POSITIONED_DELETE &#124; SQL_CA1_POSITIONED_UPDATE &#124; SQL_CA1_SELECT_FOR_UPDATE|  
|SQL_STATIC_CURSOR_ATTRIBUTES2|SQL_CA2_READ_ONLY_CONCUR &#124; SQL_CA2_OPT_VALUES_ Parallelitäts &#124; SQL_CA2_SENSITIVITY_UPDATES|  
|SQL_POS_OPERATIONS [1]|SQL_POS_POSITION|  
|SQL_POSITIONED_STATEMENTS [1]|SQL_PS_POSITIONED_DELETE &#124; SQL_PS_POSITIONED_UPDATE &#124; SQL_PS_SELECT_FOR_UPDATE|  
|SQL_ROW_UPDATES|"Y"|  
|SQL_SCROLL_CONCURRENCY [1]|SQL_SCCO_READ_ONLY &#124; SQL_SCCO_OPT_VALUES|  
|SQL_SCROLL_OPTIONS|SQL_SO_FORWARD_ONLY &#124; SQL_SO_STATIC|  
|SQL_STATIC_SENSITIVITY [1]|SQL_SS_UPDATES|  
  
 [1] wird nur verwendet, wenn die Cursor Bibliothek mit einem ODBC 2. x-Treiber verwendet wird.  
  
> [!IMPORTANT]  
>  Die Cursor Bibliothek implementiert das gleiche Cursor Verhalten, wenn für Transaktionen ein Commit oder ein Rollback als Datenquelle ausgeführt wird. Das heißt, ein Commit oder Rollback einer Transaktion, entweder durch Aufrufen von **SQLEndTran** oder mithilfe des SQL_ATTR_AUTOCOMMIT Verbindungs Attributs, kann dazu führen, dass die Datenquelle die Zugriffs Pläne löscht und die Cursor für alle Anweisungen in einer Verbindung schließt. Weitere Informationen finden Sie in den SQL_CURSOR_COMMIT_BEHAVIOR-und SQL_CURSOR_ROLLBACK_BEHAVIOR-Informationstypen in [SQLGetInfo](../../../odbc/reference/syntax/sqlgetinfo-function.md).
