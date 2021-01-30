---
description: PositionEnum
title: Positionumum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- PositionEnum
helpviewer_keywords:
- PositionEnum enumeration
ms.assetid: e69af0a5-3405-4b72-9c6e-6b188ff746fd
author: rothja
ms.author: jroth
ms.openlocfilehash: 22760113f966379d8e1705420853705114d9c362
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99170567"
---
# <a name="positionenum"></a>PositionEnum
Gibt die aktuelle Position des Daten Satz Zeigers innerhalb eines [Recordsets](./recordset-object-ado.md)an.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adposbof**|-2|Gibt an, dass sich der aktuelle Daten Satz Zeiger bei BOF befindet (d. h., die [BOF](./bof-eof-properties-ado.md) -Eigenschaft ist **true**).|  
|**adtargeof**|-3|Gibt an, dass der aktuelle Daten Satz Zeiger bei EOF ist (d. h., die [EOF](./bof-eof-properties-ado.md) -Eigenschaft ist **true**).|  
|**adPosUnknown**|-1|Gibt an, dass das **Recordset** leer ist, die aktuelle Position unbekannt ist oder der Anbieter die [AbsolutePage](./absolutepage-property-ado.md) -Eigenschaft oder die [AbsolutePosition](./absoluteposition-property-ado.md) -Eigenschaft nicht unterstützt.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoumums. Position. BOF|  
|Adoumums. Position. EOF|  
|Adoumums. Position. Unknown|  
  
## <a name="applies-to"></a>Gilt für  

:::row:::
    :::column:::
        [AbsolutePage-Eigenschaft (ADO)](./absolutepage-property-ado.md)  
    :::column-end:::
    :::column:::
        [AbsolutePosition-Eigenschaft (ADO)](./absoluteposition-property-ado.md)  
    :::column-end:::
:::row-end:::