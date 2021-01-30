---
description: Einschränkungen der DELETE-Anweisung
title: Einschränkungen der DELETE-Anweisung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- DELETE statement limitations [ODBC]
- ODBC SQL grammar, DELETE statement limitations
ms.assetid: 084761fe-e65b-4f38-ba4f-69884b2a7700
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: b188d782f82e23d031b820bba5f56a30dad414bd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99181586"
---
# <a name="delete-statement-limitations"></a>Einschränkungen der DELETE-Anweisung
Die DELETE-Anweisung wird für den Microsoft Excel-oder Text-Treiber nicht unterstützt. Beachten Sie, dass die INSERT-Anweisung für den Text Treiber unterstützt wird.  
  
 Der dBase-Treiber unterstützt das Packen einer Tabelle zum Entfernen von "gelöschten" Werten nicht.  
  
 Damit der Paradox-Treiber eine Zeile aus einer Tabelle löschen kann, muss die Tabelle über einen eindeutigen Index verfügen (Paradox-Primärschlüssel).
