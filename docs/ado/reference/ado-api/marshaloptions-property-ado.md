---
description: MarshalOptions-Eigenschaft (ADO)
title: MarshalOptions-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Recordset15::MarshalOptions
helpviewer_keywords:
- MarshalOptions property [ADO]
ms.assetid: 390c8abf-133e-40da-8b99-8f748a983e4f
author: rothja
ms.author: jroth
ms.openlocfilehash: 8797d968a342a8e68f3d3c3e19319d6a1bdc2505
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100041800"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions-Eigenschaft (ADO)
Gibt an, welche Datensätze des [Recordsets](./recordset-object-ado.md) zurück an den Server gemarshallt werden sollen.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen [marshaloptionsenum](./marshaloptionsenum.md) -Wert fest oder gibt diesen zurück. Der Standardwert ist " **admarshalall**".  
  
## <a name="remarks"></a>Bemerkungen  
 Bei Verwendung eines Client seitigen [Recordsets](./recordset-object-ado.md)werden Datensätze, die auf dem Client geändert wurden, mithilfe eines Verfahrens namens Marshalling zurück auf die mittlere Ebene oder den Webserver zurückgeschrieben. dabei handelt es sich um das Verpacken und Senden von Schnittstellen Methoden Parametern über Thread-oder Prozess Grenzen hinweg. Das Festlegen der Eigenschaft " **MarshalOptions** " kann die Leistung verbessern, wenn geänderte Remote Daten für die Aktualisierung auf die mittlere Ebene oder den Webserver gemarshallt werden.  
  
> [!NOTE]
>  **Verwendung von Remote Datendiensten** Diese Eigenschaft wird nur für ein Client seitiges **Recordset** verwendet.  
  
## <a name="applies-to"></a>Gilt für  
 [Recordset-Objekt (ADO)](./recordset-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für die MarshalOptions-Eigenschaft (VB)](./marshaloptions-property-example-vb.md)   
 [MarshalOptions-Eigenschaft – Beispiel (VC++)](./marshaloptions-property-example-vc.md)