---
description: SQLInstallTranslator-Zuordnung
title: Sqlinstalltranslator-Zuordnung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQLInstallTranslator function [ODBC], mapping
- mapping deprecated functions [ODBC], SQLInstallTranslator
ms.assetid: bcd9ba4f-7834-4bc4-876e-c7478998e524
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: b063768fed57adffd4a6e5051e5383a2ad32a943
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99202708"
---
# <a name="sqlinstalltranslator-mapping"></a>SQLInstallTranslator-Zuordnung
Wenn eine ODBC *2. x* -Anwendung **sqlinstalltranslator** über einen ODBC *3. x* -Treiber aufruft, ordnet der Treiber-Manager den Aufruf **sqlinstalltranslatorex** zu. Eine Anwendung sollte **sqlinstalltranslator** nicht im ODBC *3. x* -Treiber-Manager aufzurufen, wobei das *lpszinffile* -Argument auf einen anderen Wert als NULL festgelegt ist. Der ODBC. Die in ODBC *2. x* verwendete INF-Datei wird in ODBC *3. x* nicht mehr unterstützt, selbst aus Gründen der Abwärtskompatibilität.
