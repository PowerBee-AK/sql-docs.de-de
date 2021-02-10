---
description: Users-Collection (ADOX)
title: Users-Auflistung (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Group::Users
- Users
- Catalog::Users
helpviewer_keywords:
- Users collection [ADOX]
ms.assetid: 0a30fa74-6f10-4410-bd70-882e7c43cd46
author: rothja
ms.author: jroth
ms.openlocfilehash: 781f9eb90c621cf8daf4afb0cdf8dc4f1f7b47b4
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100049670"
---
# <a name="users-collection-adox"></a>Users-Collection (ADOX)
Enthält alle gespeicherten [Benutzer](./user-object-adox.md) Objekte eines [Katalogs](./catalog-object-adox.md) oder einer [Gruppe](./group-object-adox.md).  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Benutzer** Sammlung eines [Katalogs](./catalog-object-adox.md) stellt alle Benutzer des Katalogs dar. Die **Benutzer** Sammlung für eine [Gruppe](./group-object-adox.md) stellt nur die Benutzer dar, die über eine Mitgliedschaft in einer bestimmten Gruppe verfügen.  
  
 Die [Append](./append-method-adox-users.md) -Methode für eine **Benutzer** Sammlung ist für ADOX eindeutig. Ihre Möglichkeiten:  
  
-   Fügen Sie der Sammlung mithilfe der **Append** -Methode einen neuen Benutzer hinzu.  
  
 Die restlichen Eigenschaften und Methoden sind Standard für ADO-Auflistungen. Ihre Möglichkeiten:  
  
-   Greifen Sie mit der [Item](../ado-api/item-property-ado.md) -Eigenschaft auf einen Benutzer in der Auflistung zu.  
  
-   Gibt die Anzahl der in der Auflistung enthaltenen Benutzer mit der [count](../ado-api/count-property-ado.md) -Eigenschaft zurück.  
  
-   Entfernen Sie einen Benutzer aus der Sammlung mit der [Delete](./delete-method-adox-collections.md) -Methode.  
  
-   Aktualisieren Sie die Objekte in der Auflistung, um das Schema der aktuellen Datenbank mit [der Aktualisierungs Methode](../ado-api/refresh-method-ado.md) widerzuspiegeln.  
  
> [!NOTE]
>  Bevor ein Benutzerobjekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **Benutzer** Objekt mit demselben [Namen](./name-property-adox.md) wie das angefügte **-Objekt in** der **Benutzer** Auflistung des **Katalogs** bereits vorhanden sein.  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [Users-Collection – Eigenschaften, Methoden und Ereignisse](./users-collection-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Getberechtigungs-und setberechtigungs-Methoden Beispiel (VB)](./getpermissions-and-setpermissions-methods-example-vb.md)   
 [Catalog-Objekt (ADOX)](./catalog-object-adox.md)   
 [User-Objekt (ADOX)](./user-object-adox.md)