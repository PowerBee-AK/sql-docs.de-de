---
description: Einschränkungen für Zeichenfolgen
title: Einschränkungen für Zeichen folgen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC desktop database drivers [ODBC]
- desktop database drivers [ODBC]
ms.assetid: ec1da65f-c69d-415d-bf75-8fda8aa2b39f
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 12d02a6e69b34c13219e4bb5f00aeacfa9945cfb
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99188923"
---
# <a name="string-limitations"></a>Einschränkungen für Zeichenfolgen
Die maximale Länge einer SQL-Anweisungs Zeichenfolge beträgt 65.000 Zeichen.  
  
 Wenn der Microsoft Access-Treiber verwendet wird, werden nur SQL-92-Zeichen folgen Konstanten (in einfachen Anführungszeichen und nicht in doppelte Anführungszeichen) unterstützt.  
  
 Der senkrechter Strich (&#124;) kann nicht in einer Zeichenfolge verwendet werden, unabhängig davon, ob das Zeichen in backanführungs Zeichen eingeschlossen ist.  
  
 Für eine maximale Interoperabilität sollten Anwendungen Zeichen folgen in Parametern übergeben, anstatt Zeichen folgen in Anführungszeichen zu übergeben.
