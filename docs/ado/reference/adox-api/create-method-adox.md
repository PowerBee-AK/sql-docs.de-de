---
description: Create-Methode (ADOX)
title: Create-Methode (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Catalog::raw_Create
- _Catalog::Create
helpviewer_keywords:
- Create method [ADOX]
ms.assetid: 64f5c21c-b581-42d8-bdc7-c4f1bebaf105
author: rothja
ms.author: jroth
ms.openlocfilehash: 364af90384476b8da388c5ea5f5bfc8467ca97e5
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100054315"
---
# <a name="create-method-adox"></a>Create-Methode (ADOX)
Erstellt einen neuen Katalog.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Catalog.Create ConnectString  
```  
  
#### <a name="parameters"></a>Parameter  
 *ConnectString*  
 Ein **Zeichen** folgen Wert, der für die Verbindung mit der Datenquelle verwendet wird.  
  
## <a name="remarks"></a>Bemerkungen  
 Die **Create** -Methode erstellt eine neue ADO- [Verbindung](../ado-api/connection-object-ado.md) mit der in *ConnectString* angegebenen Datenquelle und öffnet diese. Bei erfolgreicher Ausführung wird das neue **Verbindungs** Objekt der [ActiveConnection](./activeconnection-property-adox.md) -Eigenschaft zugewiesen.  
  
 Wenn der Anbieter das Erstellen neuer Kataloge nicht unterstützt, tritt ein Fehler auf.  
  
## <a name="applies-to"></a>Gilt für  
 [Catalog-Objekt (ADOX)](./catalog-object-adox.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Create Method-Beispiel (VB)](./create-method-example-vb.md)   
 [ActiveConnection-Eigenschaft (ADOX)](./activeconnection-property-adox.md)