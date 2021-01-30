---
description: SkipLine-Methode
title: SkipLine-Methode | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Stream::raw_SkipLine
- _Stream::SkipLine
helpviewer_keywords:
- Skipline method [ADO]
ms.assetid: 0abc00fe-ee09-4c8e-b1f2-48ee9c5f3329
author: rothja
ms.author: jroth
ms.openlocfilehash: 826e90b65131453bb50cc70e3efbc3ad8796c89f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166536"
---
# <a name="skipline-method"></a>SkipLine-Methode
Überspringt beim Lesen eines [Textstreams](./stream-object-ado.md)eine gesamte Zeile.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Stream.SkipLine  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Alle Zeichen bis einschließlich des Trenn Zeichens für die nächste Zeile werden übersprungen. Standardmäßig ist der [lineseparser](./lineseparator-property-ado.md) **adCRLF**. Wenn Sie versuchen, das Überschreiten von [EOS](./eos-property.md)zu überspringen, bleibt die aktuelle Position bei **EOS** erhalten.  
  
 Die **SkipLine** -Methode wird mit Textstreams verwendet ([Type](./type-property-ado-stream.md) ist **adtypetext**).  
  
## <a name="applies-to"></a>Gilt für  
 [Stream-Objekt (ADO)](./stream-object-ado.md)