---
description: ConnectComplete- und Disconnect-Ereignis (ADO)
title: ConnectComplete-und Disconnect-Ereignisse (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Disconnect
- Connection::ConnectComplete
- ConnectComplete
- Connection::Disconnect
helpviewer_keywords:
- Disconnect event [ADO]
- ConnectComplete event [ADO]
ms.assetid: 568f5252-d069-4d99-a01b-2ada87ad1304
author: rothja
ms.author: jroth
ms.openlocfilehash: 73966677eb224c2549954f80525d88ee5622dd0c
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100026568"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete- und Disconnect-Ereignis (ADO)
Das **ConnectComplete** -Ereignis wird aufgerufen, nachdem eine Verbindung gestartet wurde. Das **Disconnect** -Ereignis wird aufgerufen, nachdem eine Verbindung beendet wurde.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
ConnectComplete pError, adStatus, pConnection  
Disconnect adStatus, pConnection  
```  
  
#### <a name="parameters"></a>Parameter  
 *pError*  
 Ein [Fehler](./error-object.md) Objekt. Es wird der Fehler beschrieben, der aufgetreten ist, wenn der Wert von *adStatus* **adstatuserrorsoccurrred** ist. Andernfalls ist es nicht festgelegt.  
  
 *adStatus*  
 Ein [EventStatus usenum](./eventstatusenum.md) -Wert, der immer **adstatuusok** zurückgibt.  
  
 Wenn **ConnectComplete** aufgerufen wird, wird dieser Parameter auf **adStatus Cancel** festgelegt, wenn ein **WillConnect** -Ereignis einen Abbruch der ausstehenden Verbindung angefordert hat.  
  
 Bevor beide Ereignisse zurückgegeben werden, legen Sie diesen Parameter auf **adStatus-unwantedevent** fest, um nachfolgende Benachrichtigungen zu verhindern. Das schließen und wieder öffnen der [Verbindung](./connection-object-ado.md) bewirkt jedoch, dass diese Ereignisse erneut auftreten.  
  
 *pConnection*  
 Das **Verbindungs** Objekt, für das dieses Ereignis gilt.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für das ADO-Ereignis Modell (VC + +)](./ado-events-model-example-vc.md)   
 [ADO-Ereignishandler – Übersicht](../../guide/data/ado-event-handler-summary.md)