---
description: Type-Eigenschaft (ADO-Stream)
title: Type-Eigenschaft (ADO-Stream) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Stream::Type
- _Stream::get_Type
- _Stream::put_Type
helpviewer_keywords:
- Type property [ADO Stream]
ms.assetid: f6a17e8c-7a28-48d0-bded-76b9e0cf7639
author: rothja
ms.author: jroth
ms.openlocfilehash: f68e21972be70369d231ede6788be5d4b200b69d
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100056445"
---
# <a name="type-property-ado-stream"></a>Type-Eigenschaft (ADO-Stream)
Gibt den Typ der im [Stream](./stream-object-ado.md) enthaltenen Daten an (binär oder Text).  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen [streamtypeenum](./streamtypeenum.md) -Wert fest, der den Typ der im **Stream** -Objekt enthaltenen Daten angibt, oder gibt ihn zurück. Der Standardwert ist **adtypetext**. Wenn jedoch Binärdaten anfänglich in einen neuen, leeren **Stream** geschrieben werden, wird der **Typ** in **adTypeBinary** geändert.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Type** -Eigenschaft ist nur Lese-/Schreibzugriff, wenn sich die aktuelle Position am Anfang des **Streams** befindet ([Position](./position-property-ado.md) ist 0) und an jeder anderen Position schreibgeschützt ist.  
  
 Die **Type** -Eigenschaft bestimmt, welche Methoden zum Lesen und Schreiben des **Streams** verwendet werden sollen. Verwenden Sie für **Textstreams** den Text "read [Text](./readtext-method.md) " und " [Write Text](./writetext-method.md)". Verwenden Sie für binäre Streams [Lese](./read-method.md) -und [Schreib](./write-method.md)Vorgänge.  
  
## <a name="applies-to"></a>Gilt für  
 [Stream-Objekt (ADO)](./stream-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [RecordType-Eigenschaft (ADO)](./recordtype-property-ado.md)   
 [Type-Eigenschaft (ADO)](./type-property-ado.md)