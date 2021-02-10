---
description: ADORecordConstruction-Schnittstelle
title: Adorecordconstruction-Schnittstelle | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ADORecordConstruction
helpviewer_keywords:
- ADORecordConstruction interface [ADO]
ms.assetid: 52a5429e-5829-455e-be3b-31f05cbecf2d
author: rothja
ms.author: jroth
ms.openlocfilehash: feb9d7d691c69cefb17054c6162caa5e803da1b0
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100035700"
---
# <a name="adorecordconstruction-interface"></a>ADORecordConstruction-Schnittstelle
Die **adorecordconstruction**-Schnittstelle wird verwendet, um ein ADO- **Datensatz** -Objekt aus einem OLE DB **Row** -Objekt in einer C/C++-Anwendung zu erstellen.  
  
 Diese Schnittstelle unterstützt die folgenden Eigenschaften:  
  
## <a name="properties"></a>Eigenschaften  
  
|Eigenschaft|BESCHREIBUNG|  
|-|-|  
|[ParentRow](./parentrow-property-ado.md)|Nur Schreibzugriff.<br />Legt den Container eines OLE DB **Row** -Objekts für dieses ADO- **Daten Satz** Objekt fest.|  
|[Zeile](./row-property-ado.md)|Lesen/Schreiben<br />Ruft ein OLE DB **Zeilen** Objekt aus/für dieses ADO- **Daten Satz** Objekt ab oder legt es fest.|  
  
## <a name="methods"></a>Methoden  
 Keine  
  
## <a name="events"></a>Ereignisse  
 Keine.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn ein OLE DB **Row** -Objekt ( `pRow` ) angegeben wird, wird die Erstellung eines ADO- **Daten Satz** Objekts ( `adoR` ) auf die folgenden drei grundlegenden Vorgänge festgestellt:  
  
1.  Erstellen Sie ein ADO- **Datensatz** -Objekt:  
  
    ```  
    _RecordPtr adoR;  
    adoRs.CreateInstance(__uuidof(_Record));  
    ```  
  
2.  Abfragen der **iadorecordconstruction** -Schnittstelle für das **Datensatz** -Objekt:  
  
    ```  
    adoRecordConstructionPtr adoRConstruct=NULL;  
    adoR->QueryInterface(__uuidof(ADORecordConstruction),  
                        (void**)&adoRConstruct);  
    ```  
  
3.  Wenden Sie die Methode **iadorecordconstruction::p ut_Row** Property an, um das OLE DB **Row** -Objekt für das ADO- **Daten** Satz Objekt festzulegen:  
  
    ```  
    IUnknown *pUnk=NULL;  
    pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);  
    adoRConstruct->put_Row(pUnk);  
    ```  
  
 Das resultierende **adoR** -Objekt stellt nun das ADO- **Daten Satz** Objekt dar, das vom OLE DB **Row** -Objekt erstellt wurde.  
  
 Ein ADO- **Datensatz** -Objekt kann auch aus dem Container eines OLE DB **Row** -Objekts erstellt werden.  
  
## <a name="requirements"></a>Requirements (Anforderungen)  
 **Version:** ADO 2,0 und höher  
  
 **Bibliothek:** msado15.dll  
  
 **UUID:** 00000567-0000-0010-8000-00AA006D2EA4