---
description: ConnectOptionEnum
title: ConnectOptionEnum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ConnectOptionEnum
helpviewer_keywords:
- ConnectOptionEnum enumeration [ADO]
ms.assetid: bff07eeb-dee3-4e4e-9b2d-d56061ea744d
author: rothja
ms.author: jroth
ms.openlocfilehash: 257dd82d5740c89fd8ca9f8f8d1969d27b9301ba
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99171429"
---
# <a name="connectoptionenum"></a>ConnectOptionEnum
Gibt an, ob die [Open](./open-method-ado-connection.md) -Methode eines [Connection](./connection-object-ado.md) -Objekts zurückgegeben werden soll, nachdem die Verbindung (synchron) oder vor (asynchron) hergestellt wurde.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adasyncconnect**|16|Öffnet die Verbindung asynchron. Das Ereignis [ConnectComplete](./connectcomplete-and-disconnect-events-ado.md) kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.|  
|**adconnectunspezifiziert**|-1|Standard. Öffnet die Verbindung synchron.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoumums. connectoption. asyncconnect|  
|Adoesums. connectoption. connectunspezifiziert|  
  
## <a name="applies-to"></a>Gilt für  
 [Open-Methode (ADO-Verbindung)](./open-method-ado-connection.md)