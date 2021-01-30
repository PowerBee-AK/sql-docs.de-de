---
description: PersistFormatEnum
title: Persistformatumum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- PersistFormatEnum
helpviewer_keywords:
- PersistFormatEnum enumeration [ADO]
ms.assetid: ebe1a2ab-e9f1-43a2-8f94-b190c9613d70
author: rothja
ms.author: jroth
ms.openlocfilehash: 25214603d009cfa8203aabe482ffdd7b511dd169
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99170577"
---
# <a name="persistformatenum"></a>PersistFormatEnum
Gibt das Format an, in dem ein [Recordset](./recordset-object-ado.md)gespeichert werden soll.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adPersistADTG**|0|Gibt das Microsoft Advanced Data TableGram (ADTG)-Format an.|  
|**adpersistado**|1|Gibt an, dass das eigene Extensible Markup Language-Format (XML) verwendet wird. Dieser Wert ist identisch mit adpersistxml und wird aus Gründen der Abwärtskompatibilität eingeschlossen.|  
|**adpersistxml**|1|Gibt Extensible Markup Language (XML)-Format an.|  
|**adpersistproviderspecific**|2|Gibt an, dass der Anbieter das **Recordset** unter Verwendung seines eigenen Formats persistent speichert.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|AdoEnums. persistformat. ADTG|  
|AdoEnums.PersistFormat.XML|  
  
## <a name="applies-to"></a>Gilt für  
 [Save-Methode](./save-method.md)