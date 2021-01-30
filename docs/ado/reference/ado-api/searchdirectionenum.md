---
description: SearchDirectionEnum
title: SearchDirectionEnum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- SearchDirectionEnum
helpviewer_keywords:
- SearchDirectionEnum enumeration [ADO]
ms.assetid: 81272ae3-2165-4f4e-adfe-9ede0368cb17
author: rothja
ms.author: jroth
ms.openlocfilehash: 957e84b3a98f0248e41a83301ef2c9a9c1943b11
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166580"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum
Gibt die Richtung einer Daten Satz Suche innerhalb eines [Recordsets](./recordset-object-ado.md)an.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adsearchrückwärts**|-1|Sucht rückwärts und beendet am Anfang des **Recordsets**. Wenn keine Entsprechung gefunden wird, wird der Daten Satz Zeiger bei [BOF](./bof-eof-properties-ado.md)positioniert.|  
|**adsearchforward**|1|Sucht vorwärts und beendet am Ende des **Recordsets**. Wenn keine Entsprechung gefunden wird, wird der Daten Satz Zeiger auf [EOF](./bof-eof-properties-ado.md)positioniert.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoumums. SearchDirection. rückwärts|  
|Adoumums. SearchDirection. Forward|  
  
## <a name="applies-to"></a>Gilt für  
 [Find-Methode (ADO)](./find-method-ado.md)