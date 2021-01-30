---
description: Cancel-Methode (RDS)
title: Cancel-Methode (RDS) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
helpviewer_keywords:
- Cancel method [RDS]
ms.assetid: 560b5b3d-fba9-4275-8920-9c3e186134f7
author: rothja
ms.author: jroth
ms.openlocfilehash: e87e8d173e1ab9aa8978ed9ab98c6a2f37a93e79
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99169071"
---
# <a name="cancel-method-rds"></a>Cancel-Methode (RDS)
Bricht die Ausführung eines ausstehenden asynchronen Methoden Aufrufes ab.  
  
> [!IMPORTANT]
>  Ab Windows 8 und Windows Server 2012 sind RDS-Server Komponenten nicht mehr im Windows-Betriebssystem enthalten (weitere Details finden Sie unter Windows 8 und [Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416) ). RDS-Client Komponenten werden in einer zukünftigen Version von Windows entfernt. Nutzen Sie diese Funktionen bei Neuentwicklungen nicht mehr, und planen Sie die Änderung von Anwendungen, die diese Funktion zurzeit verwenden. Anwendungen, die RDS verwenden, sollten zu [WCF Data Service](/dotnet/framework/wcf/)migriert werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
RDS.DataControl.Cancel  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn Sie **Abbrechen** aufrufen, wird "read [ystate](./readystate-property-rds.md) " automatisch auf " **adkreadystateloaded**" festgelegt, und das [Recordset](../ado-api/recordset-object-ado.md) ist leer.  
  
## <a name="applies-to"></a>Gilt für  
 [DataControl-Objekt (RDS)](./datacontrol-object-rds.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Cancel-Methode (Beispiel) (VBScript)](./cancel-method-example-vbscript.md)   
 [Cancel-Methode (ADO)](../ado-api/cancel-method-ado.md)   
 [CancelBatch-Methode (ADO)](../ado-api/cancelbatch-method-ado.md)   
 [CancelUpdate-Methode (ADO)](../ado-api/cancelupdate-method-ado.md)   
 [CancelUpdate-Methode (RDS)](./cancelupdate-method-rds.md)   
 [ExecuteOptions-Eigenschaft (RDS)](./executeoptions-property-rds.md)