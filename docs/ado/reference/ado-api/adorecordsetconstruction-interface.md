---
description: ADORecordsetConstruction-Schnittstelle
title: Adorecordsetconstruction-Schnittstelle | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ADORecordsetConstruction
helpviewer_keywords:
- ADORecordsetConstruction interface [ADO]
ms.assetid: 08386eba-f1f7-4879-8ffd-8733930ecb2f
author: rothja
ms.author: jroth
ms.openlocfilehash: 8f0ed083766464cccd504da7ad9270600fe0050c
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100027927"
---
# <a name="adorecordsetconstruction-interface"></a>ADORecordsetConstruction-Schnittstelle
Die **adorecordsetconstruction** -Schnittstelle wird verwendet, um ein ADO- **Recordset** -Objekt aus einem OLE DB Rowsetobjekt in einer C/C++-Anwendung zu erstellen.   
  
 Diese Schnittstelle unterstützt die folgenden Eigenschaften:  
  
## <a name="properties"></a>Eigenschaften  
  
|Eigenschaft|BESCHREIBUNG|  
|-|-|  
|[Kapitel](./chapter-property-ado.md)|Lesen/Schreiben<br />Ruft ein OLE DB **Kapitel** Objekt aus/für dieses ADO- **Recordset** -Objekt ab oder legt es fest.|  
|[RowPosition](./rowposition-property-ado.md)|Lesen/Schreiben<br />Ruft ein OLE DB **RowPosition** -Objekt von/für dieses ADO- **Recordset** -Objekt ab oder legt es fest.|  
|[Rowset](./rowset-property-ado.md)|Lesen/Schreiben<br />Ruft ein OLE DB Rowsetobjekt aus/für dieses ADO- **Recordset** -Objekt ab oder legt dieses **fest** .|  
  
## <a name="methods"></a>Methoden  
 Keine  
  
## <a name="events"></a>Ereignisse  
 Keine.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn ein OLE DB  Rowsetobjekt ( `pRowset` ) angegeben wird, wird die Erstellung eines ADO- **Recordset** -Objekts ( `adoRs` ) auf die folgenden drei grundlegenden Vorgänge festgelegt:  
  
1.  Erstellen Sie ein ADO- **Recordset** -Objekt:  
  
    ```  
    Recordset20Ptr adoRs;  
    adoRs.CreateInstance(__uuidof(Recordset));  
    ```  
  
2.  Abfragen der **IADORecordsetConstruction** -Schnittstelle für das **Recordset** -Objekt:  
  
    ```  
    adoRecordsetConstructionPtr adoRsConstruct=NULL;  
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),  
                         (void**)&adoRsConstruct);  
    ```  
  
3.  Mit der- `IADORecordsetConstruction::put_Rowset` Eigenschaft können Sie das OLE DB- `Rowset` Objekt für das ADO- `Recordset` Objekt festlegen:  
  
    ```  
    IUnknown *pUnk=NULL;  
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);  
    adoRsConstruct->put_Rowset(pUnk);  
    ```  
  
 Das resultierende `adoRs` Objekt stellt nun das ADO- **Recordset** -Objekt dar, das aus dem OLE DB Rowsetobjekt erstellt **wurde**  
  
 Sie können auch ein ADO- **Recordset** -Objekt aus einem OLE DB **Kapitel** oder einem **RowPosition** -Objekt erstellen.  
  
## <a name="requirements"></a>Requirements (Anforderungen)  
 **Version:** ADO 2,0 und höher  
  
 **Bibliothek:** msado15.dll  
  
 **UUID:** 00000283-0000-0010-8000-00AA006D2EA4  
  
## <a name="see-also"></a>Weitere Informationen  
 [Recordset-Objekt (ADO)](./recordset-object-ado.md)   
 [Rowset-Eigenschaft (ADO)](./rowset-property-ado.md)