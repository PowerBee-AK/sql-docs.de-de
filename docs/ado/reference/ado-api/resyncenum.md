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
ms.openlocfilehash: db02c56f55b577c9f74a42f43abc9a1957311c0d
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100040750"
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