---
description: Append-Methode (ADOX-Gruppen)
title: Append-Methode (ADOX-Gruppen) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Groups::raw_Append
- Groups::Append
helpviewer_keywords:
- Append method [ADOX]
ms.assetid: 56b94fc6-7ef0-4e4a-82a3-033b94c46036
author: rothja
ms.author: jroth
ms.openlocfilehash: 846475567fb15e549f96094ca55a1881d8888ce5
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100050531"
---
# <a name="append-method-adox-groups"></a>Append-Methode (ADOX-Gruppen)
Fügt der [Gruppen](./groups-collection-adox.md) Auflistung ein neues [Gruppen](./group-object-adox.md) Objekt hinzu.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Groups.Append Group  
```  
  
#### <a name="parameters"></a>Parameter  
 *Gruppe*  
 Das anzufügende **Gruppen** Objekt oder der Name der Gruppe, die erstellt und angefügt werden soll.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Groups** -Sammlung eines [Katalogs](./catalog-object-adox.md) stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Sammlung für einen [Benutzer](./user-object-adox.md) stellt nur die Gruppe dar, zu der der Benutzer gehört.  
  
 Wenn der Anbieter das Erstellen von Gruppen nicht unterstützt, tritt ein Fehler auf.  
  
> [!NOTE]
>  Vor dem Anhängen eines **Group** -Objekts an die **Groups** -Auflistung eines **User** -Objekts muss bereits ein **Gruppen** Objekt mit demselben [Namen](./name-property-adox.md) wie das angefügte-Objekt in der **Groups** -Auflistung des **Katalogs** vorhanden sein.  
  
## <a name="applies-to"></a>Gilt für  
 [Groups-Collection (ADOX)](./groups-collection-adox.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Anfügen von Gruppen und Benutzern, ChangePassword-Methoden (Beispiel) (VB)](./groups-and-users-append-changepassword-methods-example-vb.md)   
 [Append-Methode (ADOX-Spalten)](./append-method-adox-columns.md)   
 [Append-Methode (ADOX-Indizes)](./append-method-adox-indexes.md)   
 [Append-Methode (ADOX-Schlüssel)](./append-method-adox-keys.md)   
 [Append-Methode (ADOX-Prozeduren)](./append-method-adox-procedures.md)   
 [Append-Methode (ADOX-Tabellen)](./append-method-adox-tables.md)   
 [Append-Methode (ADOX-Benutzer)](./append-method-adox-users.md)   
 [Append-Methode (ADOX-Sichten)](./append-method-adox-views.md)