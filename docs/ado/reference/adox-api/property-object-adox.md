---
description: Property-Objekt (ADOX)
title: Property-Objekt (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
helpviewer_keywords:
- Property object [ADOX]
ms.assetid: 6a56def6-dbe6-4ccc-a491-8d076889f019
author: rothja
ms.author: jroth
ms.openlocfilehash: ff7c450ea1812ee5e0a9441640e2884b0394ac43
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99164071"
---
# <a name="property-object-adox"></a>Property-Objekt (ADOX)
Stellt ein Merkmal eines ADOX-Objekts dar.  
  
## <a name="remarks"></a>Bemerkungen  
 ADOX-Objekte verfügen über zwei Arten von Eigenschaften: integrierte und dynamische Eigenschaften.  
  
 Integrierte Eigenschaften sind die Eigenschaften, die für jedes neue Objekt sofort verfügbar sind. dabei wird die Syntax MyObject. Property verwendet. Sie werden nicht als Eigenschafts Objekte in der [Properties](../ado-api/properties-collection-ado.md)-Auflistung eines Objekts angezeigt, sodass Sie Ihre Werte ändern können, wenn Sie Ihre Werte ändern können.  
  
 Dynamische Eigenschaften werden vom zugrunde liegenden Datenanbieter definiert und in der Properties-Auflistung für das entsprechende ADOX-Objekt angezeigt.  Auf dynamische Eigenschaften kann nur über die Auflistung verwiesen werden, wobei die Syntax MyObject. Properties (0) oder MyObject. Properties ("Name") verwendet wird.  
  
 Beide Arten von Eigenschaften können nicht gelöscht werden.  
  
 Ein dynamisches Eigenschafts Objekt verfügt über vier eigenständig integrierte Eigenschaften:  
  
 Die [Name](../ado-api/name-property-ado.md) -Eigenschaft ist eine Zeichenfolge, die die-Eigenschaft bezeichnet.  
  
 Die [Type](../ado-api/type-property-ado.md) -Eigenschaft ist eine ganze Zahl, die den Eigenschafts Datentyp angibt.  
  
 Die [value](../ado-api/value-property-ado.md) -Eigenschaft ist eine Variante, die die Eigenschafts Einstellung enthält. Value ist die Standard Eigenschaft für ein Property-Objekt.  
  
 Die [Attribute](../ado-api/attributes-property-ado.md) -Eigenschaft ist ein langer Wert, der die Merkmale der Eigenschaft angibt, die für den Anbieter spezifisch sind.  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [ADOX-Property-Objekt – Eigenschaften, Methoden und Ereignisse](./adox-property-object-properties-methods-and-events.md)