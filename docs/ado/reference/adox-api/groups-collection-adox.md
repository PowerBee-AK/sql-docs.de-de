---
description: Groups-Collection (ADOX)
title: Groups-Auflistung (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Groups
- User::Groups
- Catalog::Groups
helpviewer_keywords:
- Groups collection [ADOX]
ms.assetid: 09aa7b0a-69d5-4564-80a7-20ad8189670f
author: rothja
ms.author: jroth
ms.openlocfilehash: 52d997496e03fccc7807c09e392568c3b4a3f4b2
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100054145"
---
# <a name="groups-collection-adox"></a>Groups-Collection (ADOX)
Enthält alle gespeicherten [Gruppen](./group-object-adox.md) Objekte eines Katalogs oder Benutzers.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Groups** -Sammlung eines [Katalogs](./catalog-object-adox.md) stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Sammlung für einen [Benutzer](./user-object-adox.md) stellt nur die Gruppe dar, zu der der Benutzer gehört.  
  
 Die [Append](./append-method-adox-groups.md) -Methode für eine **Groups** -Sammlung ist für ADOX eindeutig. Ihre Möglichkeiten:  
  
-   Fügen Sie der Sammlung mithilfe der **Append** -Methode eine neue Sicherheitsgruppe hinzu.  
  
 Die restlichen Eigenschaften und Methoden sind Standard für ADO-Auflistungen. Ihre Möglichkeiten:  
  
-   Greifen Sie mit der [Item](../ado-api/item-property-ado.md) -Eigenschaft auf eine Gruppe in der Auflistung zu.  
  
-   Gibt die Anzahl der in der Auflistung enthaltenen Gruppen mit der [count](../ado-api/count-property-ado.md) -Eigenschaft zurück.  
  
-   Entfernen Sie eine Gruppe aus der Sammlung mit der [Delete](./delete-method-adox-collections.md) -Methode.  
  
-   Aktualisieren Sie die Objekte in der Auflistung, um das aktuelle Datenbankschema mit der [Refresh](../ado-api/refresh-method-ado.md) -Methode widerzuspiegeln.  
  
> [!NOTE]
>  Vor dem Anhängen eines **Group** -Objekts an die **Groups** -Auflistung eines **User** -Objekts muss bereits ein **Gruppen** Objekt mit demselben [Namen](./name-property-adox.md) wie das angefügte-Objekt in der **Groups** -Auflistung des **Katalogs** vorhanden sein.  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [Groups-Collection – Eigenschaften, Methoden und Ereignisse](./groups-collection-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Catalog-Objekt (ADOX)](./catalog-object-adox.md)   
 [Group-Objekt (ADOX)](./group-object-adox.md)