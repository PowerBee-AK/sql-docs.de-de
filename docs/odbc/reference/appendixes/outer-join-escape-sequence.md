---
description: Escapesequenz für äußere Verknüpfungen
title: Escapesequenz für äußere Joins | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- outer join escape sequence [ODBC]
- escape sequences [ODBC], outer join
- ODBC escape sequences [ODBC], outer join
ms.assetid: 2cfd1525-6677-4d36-9b9e-730496853750
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: e25cde1a4da326d06efe23bc2f7c642e61589ff3
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99160856"
---
# <a name="outer-join-escape-sequence"></a>Escapesequenz für äußere Verknüpfungen
ODBC verwendet Escapesequenzen für äußere Joins. Die Syntax dieser Escapesequenz lautet wie folgt:  
  
```  
{oj outer-join}  
```  
  
## <a name="remarks"></a>Bemerkungen  
 In der BNF-Notation lautet die Syntax wie folgt:  
  
 *ODBC-Outer-Join-Escape* :: =  
  
 *ODBC-ESC-Initiator* OJ *Outer-Join ODBC-ESC-Terminator*  
  
 *Outer-Join* :: = *Tabellenname* [*Korrelations Name*] {Links &#124; rechts &#124; vollständig}  
  
 Äußerer Join {*Table-Name* [*Korrelations Name*] &#124; *äußerer Join*} auf  
  
 *Such*  
  
 *condition*  
  
 *Korrelations Name* :: = *benutzerdefinierter Name*  
  
 *ODBC-ESC-Initiator* :: = {  
  
 *ODBC-ESC-Terminator* :: =}  
  
 Um zu ermitteln, welche Teile dieser Anweisung unterstützt werden, ruft eine Anwendung **SQLGetInfo** mit dem SQL_OJ_CAPABILITIES Informationstyp auf. Bei äußeren Joins muss die *Such Bedingung* nur die Joinbedingung zwischen den angegebenen *Tabellennamen* enthalten.
