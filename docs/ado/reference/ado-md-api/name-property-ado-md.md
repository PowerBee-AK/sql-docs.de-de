---
description: Name-Eigenschaft (ADO MD)
title: Name-Eigenschaft (ADO MD) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Level::Name
- CubeDef::Name
- Member::Name
- Catalog::Name
- Dimension::Name
- Name
- Axis::Name
- Hierarchy::Name
helpviewer_keywords:
- Name property [ADO MD]
ms.assetid: 4a04380b-51dc-4aaf-8d25-123cdd589641
author: rothja
ms.author: jroth
ms.openlocfilehash: 96d411c00ee6f0c7d062a5bda4ca2295d4f36d5d
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100051071"
---
# <a name="name-property-ado-md"></a>Name-Eigenschaft (ADO MD)
Gibt den Namen eines Objekts an.  
  
## <a name="return-values"></a>Rückgabewerte  
 Gibt eine **Zeichenfolge** zurück und ist schreibgeschützt.  
  
## <a name="remarks"></a>Bemerkungen  
 Sie können die **Name** -Eigenschaft eines Objekts durch einen Ordinalverweis abrufen, nach dem Sie direkt auf das Objekt über den Namen verweisen können. Wenn beispielsweise `cdf.CubeDefs(0).Name` "BOSB Video Store" ergibt, können Sie diese [CubeDef](./cubedef-object-ado-md.md) als bezeichnen `cdf.CubeDefs("Bobs Video Store")` .  
  
## <a name="applies-to"></a>Gilt für  

:::row:::
    :::column:::
        [Axis-Objekt (ADO MD)](./axis-object-ado-md.md)  
        [Catalog-Objekt (ADO MD)](./catalog-object-ado-md.md)  
        [CubeDef-Objekt (ADO MD)](./cubedef-object-ado-md.md)  
    :::column-end:::
    :::column:::
        [Dimension-Objekt (ADO MD)](./dimension-object-ado-md.md)  
        [Hierarchy-Objekt (ADO MD)](./hierarchy-object-ado-md.md)  
    :::column-end:::
    :::column:::
        [Level-Objekt (ADO MD)](./level-object-ado-md.md)  
        [Member-Objekt (ADO MD)](./member-object-ado-md.md)  
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Weitere Informationen  
 [Katalog Beispiel (VB)](./catalog-example-vb.md)   
 [Caption-Eigenschaft (ADO MD)](./caption-property-ado-md.md)   
 [Description-Eigenschaft (ADO MD)](./description-property-ado-md.md)   
 [UniqueName-Eigenschaft (ADO MD)](./uniquename-property-ado-md.md)