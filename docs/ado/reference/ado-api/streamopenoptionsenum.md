---
description: StreamOpenOptionsEnum
title: StreamOpenOptionsEnum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- StreamOpenOptionsEnum
helpviewer_keywords:
- StreamOpenOptionsEnum enumeration [ADO]
ms.assetid: 85b6c57f-47ed-46ba-bd92-07882ae9e9d2
author: rothja
ms.author: jroth
ms.openlocfilehash: 5da222318b827eae05d07d7cad4a121a568d6540
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166422"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum
Gibt Optionen für das Öffnen eines Daten [Strom](./stream-object-ado.md) Objekts an. Die Werte können mit einem or-Vorgang kombiniert werden.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**Adoption-streamasync**|1|Öffnet das **Stream** -Objekt im asynchronen Modus.|  
|**"adopendstreamfromrecord"**|4|Identifiziert den Inhalt des *Quell* Parameters als bereits geöffnetes [Daten Satz](./record-object-ado.md) Objekt. Das Standardverhalten besteht darin, die *Quelle* als URL zu behandeln, die direkt auf einen Knoten in einer Baumstruktur verweist. Der Standarddaten Strom, der diesem Knoten zugeordnet ist, wird geöffnet.|  
|**"adopendstreamunspezifiziert"**|-1|Standard. Gibt an, dass das **Stream** -Objekt mit Standardoptionen geöffnet wird.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Diese Konstanten haben keine ADO/WFC-Entsprechungen.  
  
## <a name="applies-to"></a>Gilt für  
 [Open-Methode (ADO-Datenstrom)](./open-method-ado-stream.md)