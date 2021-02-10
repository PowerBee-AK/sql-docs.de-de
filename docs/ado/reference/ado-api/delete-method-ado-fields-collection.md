---
description: Delete-Methode (ADO-Fields-Collection)
title: Delete-Methode (ADO Fields-Auflistung) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Fields20::Delete
- Fields20::raw_Delete
helpviewer_keywords:
- Delete method [ADO]
ms.assetid: 25bedc25-c51c-4cab-96ce-930b959965d9
author: rothja
ms.author: jroth
ms.openlocfilehash: 9cfc2784e0a6019e4a3aaee68cb18c54b0e52fc3
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100034410"
---
# <a name="delete-method-ado-fields-collection"></a>Delete-Methode (ADO-Fields-Collection)
Löscht ein-Objekt aus der [Fields](../../../ado/reference/ado-api/fields-collection-ado.md) -Auflistung.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Fields.Delete Field  
```  
  
#### <a name="parameters"></a>Parameter  
 *Feld*  
 Eine **Variante** , die das zu löschende [Feld](../../../ado/reference/ado-api/field-object.md) Objekt festlegt. Dieser Parameter kann der Name des **Feld** Objekts oder die Ordinalposition des **Feld** Objekts selbst sein.  
  
## <a name="remarks"></a>Bemerkungen  
 Das Aufrufen der **Fields. Delete** -Methode für ein geöffnetes [Recordset](../../../ado/reference/ado-api/recordset-object-ado.md) führt zu einem Laufzeitfehler.  
  
## <a name="applies-to"></a>Gilt für  
 [Fields-Collection (ADO)](../../../ado/reference/ado-api/fields-collection-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Delete-Methode (ADO Parameters-Sammlung)](../../../ado/reference/ado-api/delete-method-ado-parameters-collection.md)   
 [Delete-Methode (ADO-Recordset)](../../../ado/reference/ado-api/delete-method-ado-recordset.md)   
 [DeleteRecord-Methode (ADO)](../../../ado/reference/ado-api/deleterecord-method-ado.md)
