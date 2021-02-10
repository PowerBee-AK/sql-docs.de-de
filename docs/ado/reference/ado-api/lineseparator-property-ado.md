---
description: LineSeparator-Eigenschaft (ADO)
title: Lineseparser-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Stream::LineSeparator
helpviewer_keywords:
- LineSeparator property [ADO]
ms.assetid: 0b20fbb8-6b83-48ec-b442-f96c8a4bafbb
author: rothja
ms.author: jroth
ms.openlocfilehash: fa50003834cf83017ec9eaf4581ed1cff7bd26bc
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100044280"
---
# <a name="lineseparator-property-ado"></a>LineSeparator-Eigenschaft (ADO)
Gibt das binäre Zeichen an, das als Zeilen Trennzeichen in [textstreamobjekten](./stream-object-ado.md) verwendet werden soll.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen [lineseparameatorsenum](./lineseparatorsenum.md) -Wert fest, der das im **Stream** verwendete Zeilen Trennzeichen angibt, oder gibt diesen zurück. Der Standardwert ist **adCRLF**.  
  
## <a name="remarks"></a>Bemerkungen  
 Mit **lineseparser** werden Zeilen beim Lesen des Inhalts eines **Textstreams** interpretiert. Zeilen können mit der [SkipLine](./skipline-method.md) -Methode übersprungen werden.  
  
 **Lineseparser** wird nur mit **textstreamobjekten** ([Typ](./type-property-ado-stream.md) : **adtypetext**) verwendet. Diese Eigenschaft wird ignoriert, wenn der **Typ** **adTypeBinary** ist.  
  
## <a name="applies-to"></a>Gilt für  
 [Stream-Objekt (ADO)](./stream-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Stream-Objekt (ADO)](./stream-object-ado.md)