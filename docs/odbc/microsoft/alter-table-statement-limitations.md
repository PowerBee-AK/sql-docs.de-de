---
description: Einschränkungen der ALTER TABLE-Anweisung
title: Einschränkungen der ALTER TABLE-Anweisung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC SQL grammar, ALTER TABLE statement limitations
- ALTER TABLE statement limitations [ODBC]
ms.assetid: f3e88f85-edf4-47cd-a822-292b106ddb34
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d36e5dfb2457a9d3453dbe3bc877c5d267731ea1
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205746"
---
# <a name="alter-table-statement-limitations"></a>Einschränkungen der ALTER TABLE-Anweisung
Wenn der dBASE-oder Paradox-Treiber verwendet wird, kann die Struktur der Tabelle nach dem Erstellen eines Indexes und einem hinzugefügten neuen Datensatz nicht von der ALTER TABLE-Anweisung geändert werden, es sei denn, der Index wird gelöscht und der Inhalt der Tabelle gelöscht.  
  
 ALTER TABLE-Anweisungen werden für Microsoft Excel-oder Text-Treiber nicht unterstützt.  
  
> [!NOTE]  
>  Wenn Sie den Paradox-Treiber verwenden, ohne den Borland-Datenbank-Engine zu implementieren, werden ALTER TABLE-Anweisungen nicht unterstützt. nur Lese-und Anfügen-Anweisungen sind zulässig.
