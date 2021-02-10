---
description: Delete-Methode (ADO-Parameters-Collection)
title: Delete-Methode (ADO Parameters-Sammlung) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _DynaCollection::Delete
- _DynaCollection::raw_Delete
helpviewer_keywords:
- Delete method [ADO]
ms.assetid: 160c575e-df63-4ade-a2d3-5fd8f72e70cc
author: rothja
ms.author: jroth
ms.openlocfilehash: 13963a0902ba0b1602b270f373a9e1f2d0e0a4cf
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100025590"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete-Methode (ADO-Parameters-Collection)
Löscht ein-Objekt aus der [Parameter](../../../ado/reference/ado-api/parameters-collection-ado.md) Auflistung.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Parameters.Delete Index  
```  
  
#### <a name="parameters"></a>Parameter  
 *Index*  
 Ein **Zeichen** folgen Wert, der den Namen des zu löschenden Objekts oder die Ordinalposition (Index) des Objekts in der Auflistung enthält.  
  
## <a name="remarks"></a>Bemerkungen  
 Mithilfe der **Delete** -Methode für eine Auflistung können Sie eines der Objekte in der Auflistung entfernen. Diese Methode ist nur in der **Parameters** -Auflistung eines [Befehls](../../../ado/reference/ado-api/command-object-ado.md) Objekts verfügbar. Wenn Sie die **Delete** -Methode aufrufen, müssen Sie die [Name](../../../ado/reference/ado-api/name-property-ado.md) -Eigenschaft des [Parameter](../../../ado/reference/ado-api/parameter-object.md) Objekts oder den zugehörigen Sammlungs Index verwenden. eine Objekt Variable ist kein gültiges Argument.  
  
## <a name="applies-to"></a>Gilt für  
 [Parameters-Collection (ADO)](../../../ado/reference/ado-api/parameters-collection-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Delete-Methode (ADO Fields-Auflistung)](../../../ado/reference/ado-api/delete-method-ado-fields-collection.md)   
 [Delete-Methode (ADO-Recordset)](../../../ado/reference/ado-api/delete-method-ado-recordset.md)   
 [DeleteRecord-Methode (ADO)](../../../ado/reference/ado-api/deleterecord-method-ado.md)
