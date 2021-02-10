---
description: Axes-Collection (ADO MD)
title: Achsen Auflistung (ADO MD) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Axes
- Cellset::Axes
helpviewer_keywords:
- Axes collection [ADO MD]
ms.assetid: 072fb21a-ec0f-4b02-9022-1cef3ad4bfff
author: rothja
ms.author: jroth
ms.openlocfilehash: a22c2fdf2ee3a8b3397e51643c728f1c860384b8
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100055835"
---
# <a name="axes-collection-ado-md"></a>Axes-Collection (ADO MD)
Enthält die [Achsen](./axis-object-ado-md.md) Objekte, die ein Cellset definieren.  
  
## <a name="remarks"></a>Bemerkungen  
 Ein [Cellset](./cellset-object-ado-md.md) -Objekt enthält eine **Achsen** Auflistung. Sobald das **Cellset** geöffnet ist, enthält diese Auflistung mindestens eine **Achse**. Eine ausführlichere Erläuterung der Verwendung von **Achsen** Objekten finden Sie im [Achsen](./axis-object-ado-md.md) Objekt.  
  
> [!NOTE]
>  Die Filter Achse eines **Cellsets** ist nicht in der **Achsen** Auflistung enthalten. Weitere Informationen finden Sie in der [FilterAxis](./filteraxis-property-ado-md.md) -Eigenschaft.  
  
 **Achsen** ist eine standardmäßige ADO-Auflistung. Mit den Eigenschaften und Methoden einer Sammlung können Sie folgende Aufgaben ausführen:  
  
-   Abrufen der Anzahl von Objekten in der Auflistung mit der [count](../ado-api/count-property-ado.md) -Eigenschaft.  
  
-   Gibt ein Objekt aus der Auflistung mit der Standard [Element](../ado-api/item-property-ado.md) Eigenschaft zurück.  
  
-   Aktualisieren Sie die Objekte in der Auflistung vom Anbieter mit der [Refresh](../ado-api/refresh-method-ado.md) -Methode.  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [Eigenschaften, Methoden und Ereignisse](./axes-collection-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Cellset-Beispiel (VB)](./cellset-example-vb.md)   
 [Axis-Objekt (ADO MD)](./axis-object-ado-md.md)