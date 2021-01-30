---
description: Procedures-Collection (ADOX)
title: Prozeduren (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Procedures
- Catalog::Procedures
helpviewer_keywords:
- Procedures collection [ADOX]
ms.assetid: dc7a38e1-93b9-4034-9af2-ff419e8fb2a3
author: rothja
ms.author: jroth
ms.openlocfilehash: c77c3eccd6cc2e61898b1619ec6255f65227384b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99169249"
---
# <a name="procedures-collection-adox"></a>Procedures-Collection (ADOX)
Enthält alle [Prozedur](./procedure-object-adox.md) Objekte eines Katalogs.  
  
## <a name="remarks"></a>Bemerkungen  
 Die [Append](./append-method-adox-procedures.md) -Methode für eine **Prozeduren** Auflistung ist für ADOX eindeutig. Ihre Möglichkeiten:  
  
-   Fügen Sie der Auflistung mithilfe der **Append** -Methode eine neue Prozedur hinzu.  
  
 Die restlichen Eigenschaften und Methoden sind Standard für ADO-Auflistungen. Ihre Möglichkeiten:  
  
-   Greifen Sie mit der [Item](../ado-api/item-property-ado.md) -Eigenschaft auf eine Prozedur in der-Auflistung zu.  
  
-   Gibt die Anzahl der in der Auflistung enthaltenen Prozeduren mit der [count](../ado-api/count-property-ado.md) -Eigenschaft zurück.  
  
-   Entfernen Sie eine Prozedur aus der Auflistung mit der [Delete](./delete-method-adox-collections.md) -Methode.  
  
-   Aktualisieren Sie die Objekte in der Auflistung, um das aktuelle Datenbankschema mit der [Refresh](../ado-api/refresh-method-ado.md) -Methode widerzuspiegeln.  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [Indexes-Collections – Eigenschaften, Methoden und Ereignisse](./indexes-collection-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für Befehls-und CommandText-Eigenschaften (VB)](./command-and-commandtext-properties-example-vb.md)   
 [Parameter Auflistung, Beispiel für Befehls Eigenschaft (VB)](./parameters-collection-command-property-example-vb.md)   
 [Prozeduren Append-Methode Beispiel (VB)](./procedures-append-method-example-vb.md)   
 [Prozeduren Delete-Methode (Beispiel) (VB)](./procedures-delete-method-example-vb.md)   
 [Prozeduren Aktualisierungs Methode (Beispiel) (VB)](./procedures-refresh-method-example-vb.md)   
 [Prozeduren: Auflistungs Eigenschaften, Methoden und Ereignisse](./procedures-collection-properties-methods-and-events.md)   
 [Catalog-Objekt (ADOX)](./catalog-object-adox.md)   
 [Procedure-Objekt (ADOX)](./procedure-object-adox.md)