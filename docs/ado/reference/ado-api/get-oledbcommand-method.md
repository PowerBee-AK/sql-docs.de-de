---
description: get_OLEDBCommand-Methode
title: get_OLEDBCommand-Methode | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
helpviewer_keywords:
- get_OLEDBCommand method [ADO]
ms.assetid: 23d551f5-3d5b-434b-ade6-fef15f1710e7
author: rothja
ms.author: jroth
ms.openlocfilehash: edd8816389088c077f43ed7b36f01ebd61010e98
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99171004"
---
# <a name="get_oledbcommand-method"></a>get_OLEDBCommand-Methode
Gibt den zugrunde liegenden OLE DB-Befehl zurück, wobei zuerst alle Parameterinformationen, die für den ADO-Befehl festgelegt wurden, an den OLE DB-Befehl  
  
## <a name="syntax"></a>Syntax  
  
```  
  
HRESULT get_OLEDBCommand(  
      IUnknown **ppOLEDBCommand  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 *ppoledbcommand*  
 vorgenommen Ein Zeiger auf einen Zeiger Speicherort, an dem der IUnknown-Zeiger für den zugrunde liegenden OLE DB Befehl geschrieben wird.  
  
## <a name="applies-to"></a>Gilt für  
 [Iadocommandconstruction](/previous-versions/windows/desktop/aa965677(v=vs.85))