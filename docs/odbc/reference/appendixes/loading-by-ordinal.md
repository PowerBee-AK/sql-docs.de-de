---
description: Laden nach Ordnungszahl
title: Laden nach Ordnungszahl | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- backward compatibility [ODBC], loading by ordinal
- compatibility [ODBC], loading by ordinal
- loading by ordinal [ODBC]
ms.assetid: 337d90ab-68eb-4940-a2f3-f7d5693ee766
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: ffb2516a79144a5ae79b21e6621882056b1f69ff
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99184378"
---
# <a name="loading-by-ordinal"></a>Laden nach Ordnungszahl
In ODBC *2. x* kann das Laden nach Ordnungszahl durchgeführt werden, um die Leistung des Verbindungs Vorgangs zu verbessern. Ein ODBC *2. x* -Treiber exportiert eine Dummy-Funktion mit der Ordinalzahl 199; Wenn Sie vom Treiber-Manager erkannt wird, werden die Adressen der ODBC-Funktionen nach Ordinalzahl, nicht nach Name aufgelöst. Diese Funktion wird weiterhin für ODBC *2. x* -Treiber unterstützt, wird aber nicht für ODBC *3. x* -Treiber unterstützt.
