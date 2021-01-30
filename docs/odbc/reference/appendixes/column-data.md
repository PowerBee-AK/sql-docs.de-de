---
description: Spaltendaten
title: Spaltendaten | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- column data [ODBC]
- ODBC cursor library [ODBC], cache
- cursor library [ODBC], cache
- cache [ODBC]
ms.assetid: 0425818c-9469-493f-9e3c-fc03d9411c5c
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 1287a4deadc6f35bf83f6c42dcebc633f6557fed
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99212347"
---
# <a name="column-data"></a>Spaltendaten
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Vermeiden Sie die Verwendung dieses Features bei der Entwicklung neuer Anwendungen, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird Microsoft empfiehlt die Verwendung der Cursor-Funktionalität des Treibers.  
  
 Die Cursor Bibliothek erstellt einen Puffer im Cache für jeden Datenpuffer, der an das Resultset mit **SQLBindCol** gebunden ist. Die Werte in diesen Puffern werden verwendet, um eine **Where** -Klausel zu erstellen, wenn Sie eine positionierte UPDATE-oder DELETE-Anweisung emuliert. Diese Puffer werden von den rowsetpuffern aktualisiert, wenn Daten aus der Datenquelle abgerufen und positionierte UPDATE-Anweisungen ausgeführt werden.  
  
 Wenn die Cursor Bibliothek den Cache aus den rowsetpuffern aktualisiert, überträgt Sie die Daten entsprechend dem in **SQLBindCol** angegebenen C-Datentyp. Wenn z. b. der C-Datentyp eines rowsetpuffers SQL_C_SLONG ist, überträgt die Cursor Bibliothek vier Byte Daten. Wenn Sie SQL_C_CHAR und *BufferLength* den Wert 10 hat, überträgt die Cursor Bibliothek 10 Bytes an Daten. Die Cursor Bibliothek führt keine Typüberprüfung oder Konvertierungen für die Daten aus, die Sie überträgt.  
  
> [!NOTE]  
>  Die Cursor Bibliothek aktualisiert Ihren Cache für eine Spalte nicht, wenn **StrLen_or_IndPtr* im entsprechenden rowsetpuffer SQL_DATA_AT_EXEC oder das Ergebnis des SQL_LEN_DATA_AT_EXEC Makros ist.  
  
 Wenn eine Spalte aktualisiert wird, stellt eine Datenquelle für Zeichendaten mit fester Länge einen leeren Wert dar, und die Binärdaten fester Länge werden bei Bedarf von NULL aufgefüllt. Beispielsweise speichert eine Datenquelle "Smith" in einer char (10)-Spalte als "Smith". Die Cursor Bibliothek kopiert Daten in den rowsetpuffern nicht, wenn diese Daten nach dem Ausführen einer positionierten Update-Anweisung in Ihren Cache kopiert werden. Wenn es für eine Anwendung erforderlich ist, dass die Werte im Cache der Cursor Bibliothek leer oder mit Nullen aufgefüllt werden, müssen die Werte in den rowsetpuffern vor dem Ausführen einer positionierten Update-Anweisung leer oder NULL aufgefüllt werden.
