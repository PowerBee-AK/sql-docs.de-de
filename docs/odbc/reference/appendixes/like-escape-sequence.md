---
description: LIKE-Escapesequenz
title: LIKE-Escapesequenz | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- ODBC escape sequences [ODBC], LIKE
- LIKE escape sequence [ODBC]
- escape sequences [ODBC], LIKE
ms.assetid: 798d75ea-be9d-4bef-b297-318bc327f1ca
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d32b0470cb2adf0960e23dac17d8cb4942f296c0
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99184395"
---
# <a name="like-escape-sequence"></a>LIKE-Escapesequenz
ODBC verwendet Escapesequenzen für die LIKE-Klausel. Die Syntax dieser Escapesequenz lautet wie folgt:  
  
```  
{'escape-character'}  
```  
  
## <a name="remarks"></a>Bemerkungen  
 In der BNF-Notation lautet die Syntax wie folgt:  
  
 *ODBC-like-Escape* :: =  
  
 *ODBC-ESC-Initiator-* *Escapezeichen*' *ODBC-ESC-Terminator* '  
  
 *Escape-Zeichen* :: =- *Zeichen*  
  
 *ODBC-ESC-Initiator* :: = {  
  
 *ODBC-ESC-Terminator* :: =}  
  
 Um zu ermitteln, ob der Treiber die like-Escapesequenz unterstützt, kann eine Anwendung **SQLGetInfo** mit dem SQL_LIKE_ESCAPE_CLAUSE Informationstyp aufrufen.
