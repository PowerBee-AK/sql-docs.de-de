---
description: RowPosition-Eigenschaft (ADO)
title: RowPosition-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ADORecordConstruction::put_RowPosition
- ADORecordConstruction::PutRowPosition
- ADORecordConstruction::GetRowPosition
- ADORecordConstruction::RowPosition
- ADORecordConstruction::get_RowPosition
helpviewer_keywords:
- RowPosition property [ADO]
ms.assetid: 9d068fed-39bf-4842-afc3-686a2af2145d
author: rothja
ms.author: jroth
ms.openlocfilehash: a836ca9dd23e6bb43d6bcf3a2707c4b523d530f4
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99166620"
---
# <a name="rowposition-property-ado"></a>RowPosition-Eigenschaft (ADO)
Ruft ein OLE DB **RowPosition** -Objekt von/in einem **adorecordsetconstruction** -Objekt ab oder legt es fest. Wenn Sie **put_RowPosition** verwenden, um das **RowPosition** -Objekt festzulegen, verwendet das resultierende **Recordset** -Objekt das **RowPosition** -Objekt, um die aktuelle Zeile zu bestimmen.  
  
 Lese-/Schreibzugriff.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT get_RowPosition([out, retval] IUnknown** ppRowPos);  
HRESULT put_RowPosition([in] IUnknown* pRowPos);  
```  
  
## <a name="parameters"></a>Parameter  
 *pprowpos*  
 Zeiger auf ein OLE DB **RowPosition** -Objekt.  
  
 *Prowpos*  
 Ein OLE DB **RowPosition** -Objekt.  
  
## <a name="return-values"></a>Rückgabewerte  
 Diese Eigenschaften Methode gibt die HRESULT-Standardwerte zurück, einschließlich S_OK und E_FAIL.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn diese Eigenschaft festgelegt ist und sich  das Rowsetobjekt für das **RowPosition** -Objekt vom Rowsetobjekt des **Recordset** -Objekts unterscheidet, überschreibt das erste das zweite.  Das gleiche Verhalten gilt auch für das aktuelle **Kapitel** der **RowPosition** .  
  
## <a name="applies-to"></a>Gilt für  
 [ADORecordsetConstruction-Schnittstelle](./adorecordsetconstruction-interface.md)