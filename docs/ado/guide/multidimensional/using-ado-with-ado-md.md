---
description: Verwenden von ADO mit ADO MD
title: Verwenden von ADO mit ADO MD | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- ADO, using with ADO MD
ms.assetid: cfae435e-2ac3-4312-8c1e-9ca4a74cd875
author: rothja
ms.author: jroth
ms.openlocfilehash: d6844590043e0f806381f35c3f74123c24a6dc30
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100032162"
---
# <a name="using-ado-with-ado-md"></a>Verwenden von ADO mit ADO MD
ADO und ADO MD sind miteinander verknüpft, aber getrennte Objekt Modelle. ADO stellt Objekte für das Herstellen einer Verbindung mit Datenquellen, das Ausführen von Befehlen, das Abrufen von Tabellendaten und Schema Metadaten in einem Tabellenformat und das Anzeigen von Anbieter Fehlerinformationen bereit. ADO MD stellt Objekte zum Abrufen mehrdimensionaler Daten und zum Anzeigen von mehrdimensionalen Schema Metadaten bereit.  
  
 Wenn Sie mit einem MDP arbeiten, können Sie sich für die Verwendung von ADO, ADO MD oder beides mit Ihrer Anwendung entscheiden. Wenn Sie auf beide Bibliotheken innerhalb Ihres Projekts verweisen, haben Sie vollständigen Zugriff auf die Funktionen, die von Ihrem MDP bereitgestellt werden.  
  
 Es ist häufig nützlich für Consumer, eine vereinfachte tabellarische Ansicht eines mehrdimensionalen Datasets zu erhalten. Hierfür können Sie das ADO- [Recordset](../../reference/ado-api/recordset-object-ado.md) -Objekt verwenden. Geben Sie die Quelle für das [Cellset](../../reference/ado-md-api/cellset-object-ado-md.md) als ***Source** _-Parameter für die [Open](../../reference/ado-api/open-method-ado-recordset.md) -Methode eines _ * Recordsets * * anstelle als Quelle für ein ADO MD **Cellset** an.  
  
 Es kann auch hilfreich sein, die Schema Metadaten in einer tabellarischen Ansicht und nicht als eine Hierarchie von Objekten anzuzeigen. Die ADO [OpenSchema](../../reference/ado-api/openschema-method.md) -Methode für das [Verbindungs](../../reference/ado-api/connection-object-ado.md) Objekt ermöglicht dem Benutzer das Öffnen eines **Recordsets** , das Schema Informationen enthält. Der **_QueryType_*_-Parameter der _* OpenSchema** -Methode verfügt über mehrere [SchemaEnum](../../reference/ado-api/schemaenum.md) -Werte, die sich speziell auf MDPs beziehen. Die Werte lauten wie folgt:  
  
-   **adschemacubes**  
  
-   **adschemadimensions**  
  
-   **adschemahierarchien**  
  
-   **adschemalevels**  
  
-   **adschemameasures**  
  
-   **"adschemamembers"**  
  
 Um ADO-Enumerationswerte mit ADO MD Eigenschaften oder Methoden zu verwenden, muss das Projekt auf die ADO-und ADO MD-Bibliotheken verweisen. Beispielsweise können Sie die ADO **adstate** -Enumerationswerte mit der ADO MD [State](../../reference/ado-md-api/state-property-ado-md.md) -Eigenschaft verwenden. Weitere Informationen zum Erstellen von Verweisen auf Bibliotheken finden Sie in der Dokumentation zu Ihrem Entwicklungs Tool.  
  
 Weitere Informationen zu den ADO-Objekten und-Methoden finden Sie in der [ADO-API-Referenz](../../reference/ado-api/ado-api-reference.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [ADO MD-Objektmodell](../../reference/ado-md-api/ado-md-object-model.md)   
 [ADO (mehrdimensional) (ADO MD)](./ado-multidimensional-ado-md.md)   
 [Übersicht über mehrdimensionale Schemas und Daten](./overview-of-multidimensional-schemas-and-data.md)   
 [Programmieren mit ADO MD](./programming-with-ado-md.md)   
 [Arbeiten mit mehrdimensionalen Daten](./working-with-multidimensional-data.md)