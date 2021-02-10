---
description: Cursor und Merkmale der Sperre
title: Cursor-und Sperr Merkmale | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- locks [ADO], characteristics
- adOpenDynamic [ADO]
- cursors [ADO], characteristics
ms.assetid: 459c29cb-4230-42bf-8cc2-f3132ccc7aba
author: rothja
ms.author: jroth
ms.openlocfilehash: cecbdd12fd98e6f58d07cfe30c6c0b8a044ed15e
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037685"
---
# <a name="cursor-and-lock-characteristics"></a>Cursor und Merkmale der Sperre
Obwohl die Merkmale eines Cursors von den Funktionen des Anbieters abhängen, gelten die folgenden vor-und Nachteile in der Regel für die verschiedenen Typen von Cursorn und sperren.  
  
|Cursor-oder Sperrentyp|Vorteile|Nachteile|  
|-------------------------|----------------|-------------------|  
|**adOpenForwardOnly**|-Geringe Ressourcenanforderungen|-Kann nicht Rückwärtsscrollen<br />-Keine Daten Parallelität|  
|**adopkostatic**|-Scrollfähig|-Keine Daten Parallelität|  
|**adOpenKeyset**|-Einige Daten Parallelität<br />-Scrollfähig|-Höhere Ressourcenanforderungen<br />-Nicht in einem getrennten Szenario verfügbar|  
|**adOpenDynamic**|-Hohe Daten Parallelität<br />-Scrollfähig|-Höchste Ressourcenanforderungen<br />-Nicht in einem getrennten Szenario verfügbar|  
|**adlockread Only**|-Geringe Ressourcenanforderungen<br />-Hochgradig skalierbar|-Daten können nicht durch Cursor aktualisiert werden.|  
|**adlockbatchoptimistische**|-Batch Updates<br />-Ermöglicht getrennte Szenarios<br />-Andere Benutzer können auf Daten zugreifen.|-Daten können von mehreren Benutzern gleichzeitig geändert werden.|  
|**adlockpessimi**|-Daten können von anderen Benutzern nicht geändert werden, während Sie gesperrt sind.|-Verhindert, dass andere Benutzer auf Daten zugreifen, während Sie gesperrt sind|  
|**adlockoptimistisch**|-Andere Benutzer können auf Daten zugreifen.|-Daten können von mehreren Benutzern gleichzeitig geändert werden.|
