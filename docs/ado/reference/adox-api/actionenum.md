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
ms.openlocfilehash: fd2104a3b334da02e9bceee3ef191baac1d66cab
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100050791"
---
# <a name="actionenum"></a>ActionEnum
Gibt den Typ der Aktion an, die ausgeführt werden soll, wenn [setberechtigungen](./setpermissions-method-adox.md) aufgerufen wird.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adaccessdeny**|3|Der Gruppe oder dem Benutzer werden die angegebenen Berechtigungen verweigert.|  
|**adaccessgrant**|1|Die Gruppe oder der Benutzer verfügt mindestens über die angeforderten Berechtigungen.|  
|**adaccesswiderruf**|4|Alle expliziten Zugriffsrechte für die Gruppe oder den Benutzer werden aufgehoben.|  
|**adaccessset**|2|Die Gruppe oder der Benutzer verfügt über genau die angeforderten Berechtigungen.|