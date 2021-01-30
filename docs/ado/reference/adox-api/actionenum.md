---
description: ActionEnum
title: Aktionumum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- ActionEnum
helpviewer_keywords:
- ActionEnum enumeration [ADOX]
ms.assetid: f948febd-c885-4621-823b-421e116fec4e
author: rothja
ms.author: jroth
ms.openlocfilehash: 35f4ddd60d4056cebbf0383aa0afb240c3ecb722
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99169663"
---
# <a name="actionenum"></a>ActionEnum
Gibt den Typ der Aktion an, die ausgeführt werden soll, wenn [setberechtigungen](./setpermissions-method-adox.md) aufgerufen wird.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adaccessdeny**|3|Der Gruppe oder dem Benutzer werden die angegebenen Berechtigungen verweigert.|  
|**adaccessgrant**|1|Die Gruppe oder der Benutzer verfügt mindestens über die angeforderten Berechtigungen.|  
|**adaccesswiderruf**|4|Alle expliziten Zugriffsrechte für die Gruppe oder den Benutzer werden aufgehoben.|  
|**adaccessset**|2|Die Gruppe oder der Benutzer verfügt über genau die angeforderten Berechtigungen.|