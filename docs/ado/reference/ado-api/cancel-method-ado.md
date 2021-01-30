---
description: Cancel-Methode (ADO)
title: Cancel-Methode (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Recordset20::Cancel
- _Record::Cancel
- _Connection::Cancel
- Command25::Cancel
- _Stream::Cancel
helpviewer_keywords:
- Cancel method [ADO]
ms.assetid: e0db4e15-6787-41e2-8f13-9e9b524d620a
author: rothja
ms.author: jroth
ms.openlocfilehash: adc282492b4c6d9a21683693154e43f1177bdca0
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99164747"
---
# <a name="cancel-method-ado"></a>Cancel-Methode (ADO)
Bricht die Ausführung eines ausstehenden asynchronen Methoden Aufrufes ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
object.Cancel  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen Methoden Aufrufs zu beenden, d. h. eine Methode, die mit der Option **adasyncconnect**, **adAsyncExecute** oder **adasyncfetch** aufgerufen wird.  
  
 In der folgenden Tabelle wird gezeigt, welche Aufgabe beendet wird, wenn Sie die **Cancel** -Methode für einen bestimmten Objekttyp verwenden.  
  
|Wenn das *Objekt* ein|Der letzte asynchrone Aufrufe dieser Methode wird beendet.|  
|----------------------|-------------------------------------------------------------|  
|[Befehl](./command-object-ado.md)|[Ausführen](./execute-method-ado-command.md)|  
|[Connection](./connection-object-ado.md)|[Ausführen](./execute-method-ado-connection.md) oder [Öffnen](./open-method-ado-connection.md)|  
|[Datensatz](./record-object-ado.md)|[CopyRecord](./copyrecord-method-ado.md), [DeleteRecord](./deleterecord-method-ado.md), [muverecord](./moverecord-method-ado.md)oder [Open](./open-method-ado-record.md)|  
|[Recordset](./recordset-object-ado.md)|[Öffnen](./open-method-ado-recordset.md)|  
|[STREAM](./stream-object-ado.md)|[Öffnen](./open-method-ado-stream.md)|  
  
## <a name="applies-to"></a>Gilt für  

:::row:::
    :::column:::
        [Command-Objekt (ADO)](./command-object-ado.md)  
        [Connection-Objekt (ADO)](./connection-object-ado.md)  
    :::column-end:::
    :::column:::
        [Record-Objekt (ADO)](./record-object-ado.md)  
        [Recordset-Objekt (ADO)](./recordset-object-ado.md)  
    :::column-end:::
    :::column:::
        [Stream-Objekt (ADO)](./stream-object-ado.md)  
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Weitere Informationen  
 [Cancel-Methode (Beispiel) (VB)](./cancel-method-example-vb.md)   
 [Cancel-Methode (Beispiel) (VBScript)](../rds-api/cancel-method-example-vbscript.md)   
 [Beispiel für eine Abbruch Methode (VC + +)](./cancel-method-example-vc.md)   
 [Cancel-Methode (RDS)](../rds-api/cancel-method-rds.md)   
 [CancelBatch-Methode (ADO)](./cancelbatch-method-ado.md)   
 [CancelUpdate-Methode (ADO)](./cancelupdate-method-ado.md)   
 [CancelUpdate-Methode (RDS)](../rds-api/cancelupdate-method-rds.md)   
 [Execute-Methode (ADO-Befehl)](./execute-method-ado-command.md)   
 [Execute-Methode (ADO-Verbindung)](./execute-method-ado-connection.md)   
 [Open-Methode (ADO-Verbindung)](./open-method-ado-connection.md)   
 [Open-Methode (ADO-Recordset)](./open-method-ado-recordset.md)