---
description: FetchComplete-Ereignis (ADO)
title: FetchComplete-Ereignis (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Recordset::ExecuteComplete
- ExecuteComplete
helpviewer_keywords:
- FetchComplete event [ADO]
ms.assetid: a28d3858-566c-468d-b070-d1de4339fbea
author: rothja
ms.author: jroth
ms.openlocfilehash: 261a3a39486dc73e95a7339906a49657a0d04634
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99171114"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete-Ereignis (ADO)
Das Ereignis **FetchComplete** wird aufgerufen, nachdem alle Datensätze in einem langwierigen asynchronen Vorgang in das [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md)abgerufen wurden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
FetchComplete pError, adStatus, pRecordset  
```  
  
#### <a name="parameters"></a>Parameter  
 *pError*  
 Ein [Fehler](../../../ado/reference/ado-api/error-object.md) Objekt. Es wird der Fehler beschrieben, der aufgetreten ist, wenn der Wert von **adStatus** **adstatuserrorsoccurrred** ist. Andernfalls ist es nicht festgelegt.  
  
 *adStatus*  
 Ein [eventstatusenum](../../../ado/reference/ado-api/eventstatusenum.md) -Statuswert. Wenn dieses Ereignis aufgerufen wird, wird dieser Parameter auf **adstatuusok** festgelegt, wenn der Vorgang, der das Ereignis verursacht hat, erfolgreich war, oder auf **adstatuuserrorsoccurrred** , wenn der Vorgang fehlgeschlagen ist.  
  
 Bevor dieses Ereignis zurückkehrt, legen Sie diesen Parameter auf **adStatus-unwantedevent** fest, um nachfolgende Benachrichtigungen zu verhindern.  
  
 *pRecordset*  
 Ein **Recordset** -Objekt. Das-Objekt, für das die Datensätze abgerufen wurden.  
  
## <a name="remarks"></a>Bemerkungen  
 Um **FetchComplete** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6,0 oder höher erforderlich.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für das ADO-Ereignis Modell (VC + +)](../../../ado/reference/ado-api/ado-events-model-example-vc.md)   
 [ADO-Ereignishandler – Übersicht](../../../ado/guide/data/ado-event-handler-summary.md)
