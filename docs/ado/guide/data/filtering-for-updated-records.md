---
description: Filtern nach aktualisierten Datensätzen
title: Filtern nach aktualisierten Datensätzen | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- filtering for updated records [ADO]
ms.assetid: 4a798921-d7bb-47c9-a252-550fd9463ec9
author: rothja
ms.author: jroth
ms.openlocfilehash: c96f0519ac3dc421fe3717bd19c00735223e3375
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100033117"
---
# <a name="filtering-for-updated-records"></a>Filtern nach aktualisierten Datensätzen
Bevor Sie UpdateBatch aufrufen, können Sie mit der Recordset-Filter Eigenschaft nur die Datensätze anzeigen, die seit dem Öffnen des Recordsets oder dem letzten Aufrufen von UpdateBatch geändert wurden. Legen Sie zu diesem Zweck Filter auf adfilterpdingrecords fest, um zu bestimmen, wie viele Datensätze aktualisiert werden, wie im Codebeispiel im nächsten Abschnitt gezeigt.  
  
## <a name="remarks"></a>Bemerkungen  
 In diesem Beispiel wird das vorherige Update Batch-Beispiel erweitert, indem das Recordset direkt vor dem Aufrufen von UpdateBatch gefiltert wird, sodass der Benutzer anzeigt, welche Datensätze geändert werden, und dass das Update abgebrochen werden kann (mithilfe der CancelBatch-Methode).  
  
```  
'BeginFilterPend  
    '...  
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText  
  
    ' Change value of Phone field for first record in Recordset, saving value  
    ' for later restoration.  
    intId = objRs1("ShipperId")  
    sPhone = objRs1("Phone")  
  
    objRs1("Phone") = "(111) 555-1111"  
  
    'Add two new records  
    For i = 0 To 1  
        objRs1.AddNew  
        objRs1(1) = "New Shipper #" & CStr((i + 1))  
        objRs1(2) = "(nnn) 555-" & i & i & i & i  
    Next i  
  
    objRs1.Filter = adFilterPendingRecords  
  
    MsgBox "There are " & objRs1.RecordCount & " records pending.", _  
            , "Filter Pending"  
  
    ' Cancel the updates  
    objRs1.CancelBatch  
'EndFilterPend  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Batchmodus](./batch-mode.md)