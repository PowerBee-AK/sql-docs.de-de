---
description: ParameterDirectionEnum
title: ParameterDirectionEnum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ParameterDirectionEnum
helpviewer_keywords:
- ParameterDirectionEnum enumeration [ADO]
ms.assetid: c66aa6e6-d4f0-4f0f-9640-e08ae6cfdef3
author: rothja
ms.author: jroth
ms.openlocfilehash: 960164c8f881c3094493f3bbc828ef7982e75280
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166889"
---
# <a name="parameterdirectionenum"></a>ParameterDirectionEnum
Gibt an, ob der [Parameter](./parameter-object.md) einen Eingabeparameter, einen Ausgabeparameter, einen Eingabe-und einen Output-Parameter oder den Rückgabewert einer gespeicherten Prozedur darstellt.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adParamInput**|1|Standard. Gibt an, dass der Parameter einen Eingabeparameter darstellt.|  
|**adparser-putoutput**|3|Gibt an, dass der Parameter sowohl einen Eingabe-als auch einen Output-Parameter darstellt.|  
|**adparamoutput**|2|Gibt an, dass der Parameter einen Output-Parameter darstellt.|  
|**adparamreturnvalue**|4|Gibt an, dass der Parameter einen Rückgabewert darstellt.|  
|**adparamunknown**|0|Gibt an, dass die Parameter Richtung unbekannt ist.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoumums. ParameterDirection. Input|  
|Adoerums. ParameterDirection. InputOutput|  
|Adoerums. ParameterDirection. Output|  
|Adoenumerations. ParameterDirection. ReturnValue|  
|Adoumums. ParameterDirection. Unknown|  
  
## <a name="applies-to"></a>Gilt für  

:::row:::
    :::column:::
        [CreateParameter-Methode (ADO)](./createparameter-method-ado.md)  
    :::column-end:::
    :::column:::
        [Direction-Eigenschaft](./direction-property.md)  
    :::column-end:::
:::row-end:::