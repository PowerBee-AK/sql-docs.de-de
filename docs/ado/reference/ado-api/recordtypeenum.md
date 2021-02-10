---
description: RecordTypeEnum
title: Recordtypeumum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- RecordTypeEnum
helpviewer_keywords:
- RecordTypeEnum enumeration [ADO]
ms.assetid: f557e537-015d-4ba7-8a41-a6f00b366a91
author: rothja
ms.author: jroth
ms.openlocfilehash: 5ddaae2256f595abe3778477e020d8f6774aacec
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100051691"
---
# <a name="recordtypeenum"></a>RecordTypeEnum
Gibt den Typ des [Daten Satz](./record-object-ado.md) Objekts an.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adsimplerecord**|0|Gibt einen *einfachen* Datensatz an (enthält keine untergeordneten Knoten).|  
|**adcollectionrecord**|1|Gibt einen *Sammlungs* Daten Satz an (enthält untergeordnete Knoten).|  
|**adrecordunknown**|-1|Gibt an, dass der Typ dieses **Datensatzes** unbekannt ist.|  
|**adstructdoc**|2|Gibt eine besondere Art von *Sammlungs* Daten Satz an, der com-strukturierte Dokumente darstellt.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Diese Konstanten haben keine ADO/WFC-Entsprechungen.  
  
## <a name="applies-to"></a>Gilt für  
 [RecordType-Eigenschaft (ADO)](./recordtype-property-ado.md)