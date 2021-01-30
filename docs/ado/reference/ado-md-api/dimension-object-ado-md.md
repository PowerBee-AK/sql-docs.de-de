---
description: Dimension-Objekt (ADO MD)
title: Dimensions Objekt (ADO MD) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Dimension
helpviewer_keywords:
- Dimension object [ADO MD]
ms.assetid: 66adbbd2-23a3-4c19-a91b-84c31309aa1b
author: rothja
ms.author: jroth
ms.openlocfilehash: 8a8738c6e5143a8fc23da2c008a01b28db36ee04
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99174281"
---
# <a name="dimension-object-ado-md"></a>Dimension-Objekt (ADO MD)
Stellt eine der Dimensionen eines mehrdimensionalen Cubes dar, der mindestens eine Hierarchien von Membern enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Mit den Auflistungen und Eigenschaften eines **Dimensions** Objekts können Sie folgende Aufgaben ausführen:  
  
-   Identifizieren Sie die **Dimension** mit den Eigenschaften " [Name](./name-property-ado-md.md) " und " [UniqueName](./uniquename-property-ado-md.md) ".  
  
-   Gibt eine sinnvolle Zeichenfolge zurück, die die **Dimension** mit der [Description](./description-property-ado-md.md) -Eigenschaft beschreibt.  
  
-   Gibt die [Hierarchie](./hierarchy-object-ado-md.md) Objekte zurück, die die **Dimension** mit der [Hierarchien](./hierarchies-collection-ado-md.md) -Auflistung bilden.  
  
-   Verwenden Sie die standardmäßige ADO [Properties](../ado-api/properties-collection-ado.md) -Auflistung, um zusätzliche Informationen über das **Dimensions** Objekt zu erhalten.  
  
 Die **Properties** -Auflistung enthält vom Anbieter bereitgestellte Eigenschaften. In der folgenden Tabelle sind die verfügbaren Eigenschaften aufgeführt. Die tatsächliche Eigenschaften Liste kann je nach Implementierung des Anbieters abweichen. Eine ausführlichere Liste der verfügbaren Eigenschaften finden Sie in der Dokumentation für Ihren Anbieter.  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|CatalogName|Der Name des Katalogs, zu dem dieser Cube gehört.|  
|CubeName|Der Name des Cubes.|  
|DefaultHierarchy|Der eindeutige Name der Standard Hierarchie.|  
|BESCHREIBUNG|Eine aussagekräftige Beschreibung des Cubes.|  
|DimensionCaption|Eine Bezeichnung oder Beschriftung, die der Dimension zugeordnet ist.|  
|DimensionCardinality|Die Anzahl der Elemente in der Dimension.|  
|DimensionGUID|Die GUID der Dimension.|  
|DimensionName|Der Name der Dimension.|  
|Dimensionordinal|Die Ordinalzahl der Dimension in der Gruppe von Dimensionen, die den Cube bilden.|  
|DimensionType|Der Dimensionstyp.|  
|Dimensionuniquename|Der eindeutige Name der Dimension.|  
|SchemaName|Der Name des Schemas, zu dem dieser Cube gehört.|  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [Eigenschaften, Methoden und Ereignisse](./dimension-object-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [CubeDef-Beispiel (VBScript)](./cubedef-example-vbscript.md)   
 [CubeDef-Objekt (ADO MD)](./cubedef-object-ado-md.md)   
 [Dimensions Auflistung (ADO MD)](./dimensions-collection-ado-md.md)   
 [Hierarchien-Auflistung (ADO MD)](./hierarchies-collection-ado-md.md)   
 [Properties-Collection (ADO)](../ado-api/properties-collection-ado.md)