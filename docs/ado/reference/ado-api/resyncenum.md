---
description: ResyncEnum
title: ResyncEnum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ResyncEnum
helpviewer_keywords:
- ResyncEnum enumeration [ADO]
ms.assetid: d3df2c90-e570-4c40-a79a-25b3448a009c
author: rothja
ms.author: jroth
ms.openlocfilehash: c20965a348227583580bb75a807e792f74a9e967
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166632"
---
# <a name="resyncenum"></a>ResyncEnum
Gibt an, ob zugrunde liegende Werte durch einen Rückruf von [Resync](./resync-method.md)überschrieben werden.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adResyncAllValues**|2|Standard. Überschreibt Daten, und ausstehende Updates werden abgebrochen.|  
|**adresyncunderlyingvalues**|1|Daten werden nicht überschrieben, und ausstehende Updates werden nicht abgebrochen.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoenumerations. Resync. AllValues|  
|Adoenumerations. Resync. underlyingvalues|  
  
## <a name="applies-to"></a>Gilt für  
 [Resync-Methode](./resync-method.md)