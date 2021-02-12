---
description: CubeDef-Objekt (ADO MD)
title: CubeDef-Objekt (ADO MD) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- CubeDef
helpviewer_keywords:
- CubeDef object [ADO MD]
ms.assetid: feb2581c-fc41-471c-bb69-29f8a55fda70
author: rothja
ms.author: jroth
ms.openlocfilehash: b9f25f238fd8c0637f86ff7fdf5d9fc17320fdf7
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100054815"
---
# <a name="cubedef-object-ado-md"></a>CubeDef-Objekt (ADO MD)
Stellt einen Cube aus einem mehrdimensionalen Schema dar, der einen Satz verwandter Dimensionen enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Mit den Auflistungen und Eigenschaften eines **CubeDef** -Objekts können Sie folgende Aufgaben ausführen:  
  
-   Identifizieren Sie eine **CubeDef** mit der [Name](./name-property-ado-md.md) -Eigenschaft.  
  
-   Gibt eine Zeichenfolge zurück, die den Cube mit der [Description](./description-property-ado-md.md) -Eigenschaft beschreibt.  
  
-   Gibt die Dimensionen zurück, die den Cube mit der [Dimensions](./dimensions-collection-ado-md.md) Auflistung bilden.  
  
-   Rufen Sie zusätzliche Informationen über die **CubeDef** mit der standardmäßigen ADO [Properties](../ado-api/properties-collection-ado.md) -Sammlung ab.  
  
 Die **Properties** -Auflistung enthält vom Anbieter bereitgestellte Eigenschaften. In der folgenden Tabelle sind die verfügbaren Eigenschaften aufgeführt. Die tatsächliche Eigenschaften Liste kann je nach Implementierung des Anbieters abweichen. Eine ausführlichere Liste der verfügbaren Eigenschaften finden Sie in der Dokumentation für Ihren Anbieter.  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|CatalogName|Der Name des Katalogs, zu dem dieser Cube gehört.|  
|CreatedOn|Das Datum und die Uhrzeit der Erstellung des Cubes.|  
|Cubeguid|Die Cube-GUID.|  
|CubeName|Der Name des Cubes.|  
|Cubetype|Der Typ des Cubes.|  
|Dataupdatedby|Die Benutzer-ID der Person, die das letzte Datenupdate durchgeführt hat.|  
|BESCHREIBUNG|Eine aussagekräftige Beschreibung des Cubes.|  
|LastSchemaUpdate|Datum und Uhrzeit des letzten Schema Updates.|  
|SchemaName|Der Name des Schemas, zu dem dieser Cube gehört.|  
|Schemaupdatedby|Die Benutzer-ID der Person, die die letzte Schema Aktualisierung durchgeführt hat.|  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [Eigenschaften, Methoden und Ereignisse](./cubedef-object-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [CubeDef-Beispiel (VBScript)](./cubedef-example-vbscript.md)   
 [Catalog-Objekt (ADO MD)](./catalog-object-ado-md.md)   
 [CubeDefs-Sammlung (ADO MD)](./cubedefs-collection-ado-md.md)   
 [Dimensions Auflistung (ADO MD)](./dimensions-collection-ado-md.md)   
 [Properties-Collection (ADO)](../ado-api/properties-collection-ado.md)