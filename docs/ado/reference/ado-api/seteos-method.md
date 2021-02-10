---
description: SetEOS-Methode
title: '*-Methode | Microsoft-Dokumentation'
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Stream::raw_SetEOS
- _Stream::SetEOS
helpviewer_keywords:
- SetEOS method [ADO]
ms.assetid: 707c18ca-6a56-4970-bbd6-ae1fb86a0b8a
author: rothja
ms.author: jroth
ms.openlocfilehash: a68804b31f36c108096b5f0bb6b3b1d20b4109cd
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100040570"
---
# <a name="seteos-method"></a>SetEOS-Methode
Legt die Position fest, die das Ende des Streams ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Stream.SetEOS  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Der Wert der [EOS](./eos-property.md) -Eigenschaft wird durch die aktuelle [Position](./position-property-ado.md) am Ende des **Streams aktualisiert.** Alle Bytes oder Zeichen, die der aktuellen Position folgen, werden abgeschnitten.  
  
 Da [Write](./write-method.md), Write- [Text](./writetext-method.md)und [CopyTo](./copyto-method-ado.md) keine zusätzlichen Werte in vorhandenen **Streamobjekten** kürzen, können Sie diese Bytes oder Zeichen abschneiden, indem Sie die neue Streamende-Position mit **SetEOS** festlegen.  
  
> [!CAUTION]
>  Wenn Sie **EOS** auf eine Position vor dem eigentlichen Ende des Streams festlegen, verlieren Sie alle Daten nach der neuen **EOS** -Position.  
  
## <a name="applies-to"></a>Gilt für  
 [Stream-Objekt (ADO)](./stream-object-ado.md)