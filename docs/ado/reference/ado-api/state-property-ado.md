---
description: State-Eigenschaft (ADO)
title: State-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Command25::State
helpviewer_keywords:
- State property [ADO]
ms.assetid: 0b993bac-2653-40b1-bcbb-5b57b6aae2bf
author: rothja
ms.author: jroth
ms.openlocfilehash: 7357d21aa58bca15e1fbbeb3c9cec542ef40ce8b
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100051321"
---
# <a name="state-property-ado"></a>State-Eigenschaft (ADO)
Gibt für alle anwendbaren Objekte an, ob der Status des Objekts geöffnet oder geschlossen ist. Wenn das-Objekt eine asynchrone Methode ausführt, gibt an, ob der aktuelle Zustand des Objekts eine Verbindung herstellt, wird ausgeführt oder abgerufen wird.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt einen **Long** -Wert zurück, der ein [objectstateenum](./objectstateenum.md) -Wert sein kann. Der Standardwert ist " **adStatus eclosed**".  
  
## <a name="remarks"></a>Bemerkungen  
 Sie können die **State** -Eigenschaft verwenden, um den aktuellen Status eines bestimmten Objekts zu einem beliebigen Zeitpunkt zu bestimmen.  
  
 Die **State** -Eigenschaft des Objekts kann eine Kombination von Werten aufweisen. Wenn z. b. eine-Anweisung ausgeführt wird, hat diese Eigenschaft den kombinierten Wert **adstateopen** und **adstateausführungs**.  
  
 Die **State** -Eigenschaft ist schreibgeschützt.  
  
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
 [Beispiel für ConnectionString, ConnectionTimeout und State Properties (VB)](./connectionstring-connectiontimeout-and-state-properties-example-vb.md)   
 [Beispiel für ConnectionString, ConnectionTimeout und State Properties (VC + +)](./connectionstring-connectiontimeout-and-state-properties-example-vc.md)