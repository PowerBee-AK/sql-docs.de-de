---
description: View-Objekt (ADOX)
title: View-Objekt (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- View
helpviewer_keywords:
- View object [ADOX]
ms.assetid: 653421ce-7b94-43d0-9bc6-4900f8f2af45
author: rothja
ms.author: jroth
ms.openlocfilehash: 227a52fb1ee89777d1e198e96e253ef8dd5bb979
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100049660"
---
# <a name="view-object-adox"></a>View-Objekt (ADOX)
Stellt einen gefilterten Satz von Datensätzen oder eine virtuelle Tabelle dar. Bei Verwendung in Verbindung mit dem ADO- [Befehls](../ado-api/command-object-ado.md) Objekt kann das **View** -Objekt zum Hinzufügen, löschen oder Ändern von Sichten verwendet werden.  
  
## <a name="remarks"></a>Bemerkungen  
 Eine Sicht ist eine virtuelle Tabelle, die aus anderen Datenbanktabellen oder Sichten erstellt wurde. Mit dem **View** -Objekt können Sie eine Ansicht erstellen, ohne die "Create View"-Syntax des Anbieters kennen oder verwenden zu müssen.  
  
 Mit den Eigenschaften eines **Ansichts** Objekts können Sie folgende Aktionen ausführen:  
  
-   Identifizieren Sie die Sicht mit der [Name](./name-property-adox.md) -Eigenschaft.  
  
-   Geben Sie das ADO- **Befehls** Objekt an, das verwendet werden kann, um Sichten mit der [Command](./command-property-adox.md) -Eigenschaft hinzuzufügen, zu löschen oder zu ändern.  
  
-   Gibt Datumsinformationen mit den Eigenschaften [DateCreated](./datecreated-property-adox.md) und [DateModified](./datemodified-property-adox.md) zurück.  
  
 Dieser Abschnitt enthält das folgende Thema.  
  
-   [View-Objekt – Eigenschaften, Methoden und Ereignisse](./view-object-properties-methods-and-events.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für Sichten und Fields-Auflistungen (VB)](./views-and-fields-collections-example-vb.md)   
 [Beispiele für die Append-Methode (VB)](./views-append-method-example-vb.md)   
 [Views-Auflistung, CommandText-Eigenschafts Beispiel (VB)](./views-collection-commandtext-property-example-vb.md)   
 [Sichten Delete-Methode (Beispiel) (VB)](./views-delete-method-example-vb.md)   
 [Views-Collection (ADOX)](./views-collection-adox.md)