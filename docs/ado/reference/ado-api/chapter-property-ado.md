---
description: Chapter-Eigenschaft (ADO)
title: Chapter-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ADORecordsetConstruction::Chapter
- ADORecordsetConstruction::put_Chapter
- ADORecordsetConstruction::get_Chapter
helpviewer_keywords:
- Chapter property [ADO]
ms.assetid: 8aa90cb0-f588-4141-9dc9-3b22918394ee
author: rothja
ms.author: jroth
ms.openlocfilehash: e570ba46c7e890d0bf5123b50d2d59ce72d5f8a0
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100035519"
---
# <a name="chapter-property-ado"></a>Chapter-Eigenschaft (ADO)
Ruft ein OLE DB **Kapitel** Objekt aus/für ein [adorecordsetconstruction-Schnittstellen](./adorecordsetconstruction-interface.md) Objekt ab oder legt es fest. Wenn Sie **put_Chapter** verwenden, um das **Kapitel** Objekt festzulegen, wird eine Teilmenge von Zeilen in ein ADO- [Recordset-Objekt](./recordset-object-ado.md) Objekt umgewandelt. Dadurch wird das aktuelle Kapitel des Rowsetobjekt **fest** gelegt. Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT get_Chapter([out, retval] long* plChapter);  
HRESULT put_Chapter([in] long lChapter);  
```  
  
## <a name="parameters"></a>Parameter  
 *plchapter*  
 Zeiger auf das Handle eines Kapitels.  
  
 *Lchapter*  
 Handle eines Kapitels.  
  
## <a name="return-values"></a>Rückgabewerte  
 Diese Eigenschaften Methode gibt die HRESULT-Standardwerte zurück, einschließlich S_OK und E_FAIL.  
  
## <a name="applies-to"></a>Gilt für  
 [ADORecordsetConstruction-Schnittstelle](./adorecordsetconstruction-interface.md)