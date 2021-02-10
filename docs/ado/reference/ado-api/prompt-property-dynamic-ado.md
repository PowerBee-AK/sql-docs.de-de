---
description: Prompt – dynamische Eigenschaft (ADO)
title: Eingabeaufforderung Property-Dynamic (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
helpviewer_keywords:
- Prompt property [ADO]
ms.assetid: c4f001b5-8d16-4d39-a42e-c0e2faaaceaf
author: rothja
ms.author: jroth
ms.openlocfilehash: ab4d7c462e0e205050eed2b873a0071ac82ea936
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100040970"
---
# <a name="prompt-property-dynamic-ado"></a>Prompt – dynamische Eigenschaft (ADO)
Gibt an, ob der OLE DB Anbieter den Benutzer zur Eingabe von Initialisierungs Informationen auffordern soll.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen [connectpromptenum](./connectpromptenum.md) -Wert fest und gibt ihn zurück.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Eingabeaufforderung** ist eine dynamische Eigenschaft, die vom OLE DB Anbieter an die [Eigenschaften](./properties-collection-ado.md) Auflistung des [Verbindungs](./connection-object-ado.md) Objekts angehängt werden kann. Um Initialisierungs Informationen einzugeben, wird OLE DB Anbietern in der Regel ein Dialogfeld für den Benutzer angezeigt.  
  
 Dynamische Eigenschaften eines [Verbindungs](./connection-object-ado.md) Objekts gehen verloren, wenn die **Verbindung** geschlossen wird. Die **prompt** -Eigenschaft muss zurückgesetzt werden, bevor die **Verbindung** erneut geöffnet wird, um einen anderen Wert als den Standardwert zu verwenden.  
  
> [!NOTE]
>  Geben Sie nicht an, dass der Anbieter den Benutzer in Szenarios auffordern soll, in denen der Benutzer nicht auf das Dialogfeld reagieren kann. Der Benutzer kann beispielsweise nicht Antworten, wenn die Anwendung auf einem Server System statt auf dem Client des Benutzers ausgeführt wird oder wenn die Anwendung auf einem System ausgeführt wird, auf dem kein Benutzer angemeldet ist. In diesen Fällen wartet die Anwendung unbegrenzt auf eine Antwort und scheint eine Sperre zu erhalten.  
  
## <a name="usage"></a>Verwendung  
  
```  
Set cn = New Connection  
cn.Provider = "SQLOLEDB"  
cn.Properties("Prompt") = adPromptNever    ' do not prompt the user  
```  
  
## <a name="applies-to"></a>Gilt für  
 [Connection-Objekt (ADO)](./connection-object-ado.md)