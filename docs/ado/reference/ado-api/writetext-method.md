---
description: WriteText-Methode
title: Write Text-Methode | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Stream::raw_WriteText
- _Stream::WriteText
helpviewer_keywords:
- WriteText method [ADO]
ms.assetid: 7a669048-13f4-4574-a2b1-985e089729d5
author: rothja
ms.author: jroth
ms.openlocfilehash: b4c05ab892ce442db5eefefddf3eb0796af5dec9
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166247"
---
# <a name="writetext-method"></a>WriteText-Methode
Schreibt eine angegebene Text Zeichenfolge in ein Daten [Strom](./stream-object-ado.md) Objekt.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Stream.WriteText Data, Options  
```  
  
#### <a name="parameters"></a>Parameter  
 *Daten*  
 Ein **Zeichen** folgen Wert, der den Text in zu schreibenden Zeichen enthält.  
  
 *Optionen*  
 Optional. Ein [streamschreibwert](./streamwriteenum.md) , der angibt, ob ein Zeilen Trennzeichen am Ende der angegebenen Zeichenfolge geschrieben werden muss.  
  
## <a name="remarks"></a>Bemerkungen  
 Angegebene Zeichen folgen werden in das **Stream** -Objekt geschrieben, ohne dass dazwischen liegende Leerzeichen oder Zeichen zwischen den einzelnen Zeichen folgen liegen  
  
 Die aktuelle [Position](./position-property-ado.md) wird auf das Zeichen festgelegt, das den geschriebenen Daten folgt. Die Methode " **Write Text** " schneidet den Rest der Daten in einem Stream nicht ab. Wenn Sie diese Zeichen abschneiden möchten [, nennen Sie](./seteos-method.md)"*".  
  
 Wenn Sie über die aktuelle [EOS](./eos-property.md) -Position hinaus schreiben, wird die [Größe](./size-property-ado-stream.md) des **Streams** um alle neuen Zeichen erweitert, und **EOS** wechselt zum neuen letzten Byte im **Stream**.  
  
> [!NOTE]
>  Die Methode " **Write Text** " wird mit Textstreams verwendet ([Typ](./type-property-ado-stream.md) : **adtypetext**). Verwenden Sie für binäre Datenströme (**Typ** : **adTypeBinary**) " [Write](./write-method.md)".  
  
## <a name="applies-to"></a>Gilt für  
 [Stream-Objekt (ADO)](./stream-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Write-Methode](./write-method.md)