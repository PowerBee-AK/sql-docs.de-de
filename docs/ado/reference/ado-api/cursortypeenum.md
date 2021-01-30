---
description: CursorTypeEnum
title: Cursor typeumum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- CursorTypeEnum
helpviewer_keywords:
- CursorTypeEnum enumeration [ADO]
ms.assetid: ffc6e245-4471-42ae-84dd-e85bddfce983
author: rothja
ms.author: jroth
ms.openlocfilehash: 16c4d140efef977e3773e48dfc4f8797fda22dc5
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99171324"
---
# <a name="cursortypeenum"></a>CursorTypeEnum
Gibt den Typ des Cursors an, der in einem [Recordset](./recordset-object-ado.md) -Objekt verwendet wird.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adOpenDynamic**|2|Verwendet einen dynamischen Cursor. Ergänzungen, Änderungen und Löschungen durch andere Benutzer sind sichtbar, und alle Arten von Verschiebungen durch das **Recordset** sind zulässig, mit Ausnahme von Lesezeichen, wenn der Anbieter Sie nicht unterstützt.|  
|**adOpenForwardOnly**|0|Standard. Verwendet einen Vorwärts Cursor. Identisch mit einem statischen Cursor, mit dem Unterschied, dass Sie nur vorwärts durch Datensätze scrollen können. Dadurch wird die Leistung verbessert, wenn nur ein **Recordset** durchlaufen werden muss.|  
|**adOpenKeyset**|1|Verwendet einen Keysetcursor. Wie bei einem dynamischen Cursor, **mit dem unter** schied, dass Sie keine Datensätze sehen können, die von anderen Benutzern hinzugefügt werden, auch wenn Datensätze, die von anderen Benutzern gelöscht werden, Datenänderungen durch andere Benutzer sind weiterhin sichtbar.|  
|**adopkostatic**|3|Verwendet einen statischen Cursor, bei dem es sich um eine statische Kopie eines Satzes von Datensätzen handelt, die Sie verwenden können, um Daten zu suchen oder Berichte zu generieren. Ergänzungen, Änderungen oder Löschungen durch andere Benutzer sind nicht sichtbar.|  
|**adopunspezifiziert**|-1|Gibt den Typ des Cursors nicht an.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoerums. Cursor Type. Dynamic|  
|Adoerums. Cursor Type. ForwardOnly|  
|AdoEnums. Cursor Type. Keyset|  
|Adoerums. Cursor Type. static|  
|Adoerums. Cursor Type. nicht angegeben|  
  
## <a name="applies-to"></a>Gilt für  
 [CursorType-Eigenschaft (ADO)](./cursortype-property-ado.md)