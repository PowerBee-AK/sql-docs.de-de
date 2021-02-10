---
description: InheritTypeEnum
title: Ererttypep | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- InheritTypeEnum
helpviewer_keywords:
- InheritTypeEnum enumeration [ADOX]
ms.assetid: c2f6ce79-c4b3-4d40-ac95-21025208f991
author: rothja
ms.author: jroth
ms.openlocfilehash: ef61a93080846e8fc65a02e592ca3b171c1f92bb
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100049980"
---
# <a name="inherittypeenum"></a>InheritTypeEnum
Gibt an, wie Objekte Berechtigungen erben, die mit [setberechtigungen](./setpermissions-method-adox.md)festgelegt sind.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adgeerbt both**|3|Beide Objekte und andere Container, die im primären Objekt enthalten sind, erben den Eintrag.|  
|**adgeerbt-Container**|2|Andere Container, die im primären Objekt enthalten sind, erben den Eintrag.|  
|**adgeerbt None**|0|Standard. Es erfolgt keine Vererbung.|  
|**advererbt nopropagate**|4|Die Flags **advereritobjects** und **adgeerbt Containers** werden nicht an einen geerbten Eintrag weitergegeben.|  
|**advereritobjects**|1|Nicht-Container-Objekte im Container erben die Berechtigungen.|  
  
## <a name="applies-to"></a>Gilt für  
 [SetPermissions-Methode (ADOX)](./setpermissions-method-adox.md)