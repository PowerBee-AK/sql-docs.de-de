---
description: NumericScale-Eigenschaft (ADO)
title: NumericScale-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Parameter::NumericScale
- Field20::NumericScale
helpviewer_keywords:
- NumericScale property [ADO]
ms.assetid: 29a02992-64be-4fcd-be13-445cba205893
author: rothja
ms.author: jroth
ms.openlocfilehash: 3164dcc61165171ff0d1c33956f152bcb65f33b1
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99170740"
---
# <a name="numericscale-property-ado"></a>NumericScale-Eigenschaft (ADO)
Gibt die Skala numerischer Werte in einem [Parameter](./parameter-object.md) -oder [Feld](./field-object.md) Objekt an.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen **Bytewert** fest, der die Anzahl der Dezimalstellen angibt, auf die numerische Werte aufgelöst werden, oder gibt ihn zurück.  
  
## <a name="remarks"></a>Bemerkungen  
 Verwenden Sie die **NumericScale** -Eigenschaft, um zu bestimmen, wie viele Ziffern rechts vom Dezimaltrennzeichen verwendet werden, um Werte für einen numerischen **Parameter** oder **Feld** Objekt darzustellen.  
  
 Bei **Parameter** Objekten ist die **NumericScale** -Eigenschaft Lese-/Schreibzugriff.  
  
 Für ein **Feld** Objekt ist **NumericScale** normalerweise schreibgeschützt. Bei neuen **Feld** Objekten, die an die [Fields](./fields-collection-ado.md) -Auflistung eines [Datensatzes](./record-object-ado.md)angehängt wurden, ist **NumericScale** jedoch nur Lese-/Schreibzugriff, nachdem die [value](./value-property-ado.md) -Eigenschaft für das **Feld** angegeben wurde und der Datenanbieter das neue **Feld** erfolgreich hinzugefügt hat, indem die [Update](./update-method.md) -Methode der [Fields](./fields-collection-ado.md) -Auflistung aufgerufen wurde.  
  
## <a name="applies-to"></a>Gilt für  

:::row:::
    :::column:::
        [Field-Objekt](./field-object.md)  
    :::column-end:::
    :::column:::
        [Parameter-Objekt](./parameter-object.md)  
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für NumericScale und Precision Properties (VB)](./numericscale-and-precision-properties-example-vb.md)   
 [Beispiel für NumericScale und Precision Properties (VC + +)](./numericscale-and-precision-properties-example-vc.md)   
 [Precision-Eigenschaft (ADO)](./precision-property-ado.md)