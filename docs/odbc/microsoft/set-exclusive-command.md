---
description: SET EXCLUSIVE-Befehl
title: Exklusiven Befehl festlegen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SET EXCLUSIVE command [ODBC]
ms.assetid: d4fe12c5-7e8b-4d20-9ea4-2bcaffb271f2
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 43cd58e5e9f714de0defe36cea020ccb96ac3efa
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99208623"
---
# <a name="set-exclusive-command"></a>SET EXCLUSIVE-Befehl
Gibt an, ob Tabellen Dateien für exklusive oder freigegebene Verwendung in einem Netzwerk geöffnet werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
SET EXCLUSIVE ON | OFF  
```  
  
## <a name="arguments"></a>Argumente  
 EIN  
 Beschränkt den Zugriff auf eine Tabelle, die in einem Netzwerk geöffnet wurde, auf den Benutzer, der Sie geöffnet hat. Der Zugriff auf die Tabelle ist für andere Benutzer im Netzwerk nicht möglich. Wenn Sie exklusiv festlegen, wird auch verhindert, dass alle anderen Benutzer schreibgeschützten Zugriff haben.  
  
 OFF  
 (Standardeinstellung für den Treiber; die Standardwerte für Visual FoxPro sind für die globale Daten Sitzung aktiviert und für eine private Daten Sitzung deaktiviert.) Ermöglicht, dass eine Tabelle, die in einem Netzwerk geöffnet ist, von jedem Benutzer im Netzwerk freigegeben und geändert werden kann.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn Sie die Einstellung von Set Exclusive ändern, ändert sich der Status der zuvor geöffneten Tabellen nicht. Wenn z. b. eine Tabelle geöffnet wird, die auf ON festgelegt ist, und Set Exclusive später in Off geändert wird, behält die Tabelle ihren exklusiven Verwendungs Status bei.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Einrichten von ODBC-Visual FoxPro (Dialogfeld)](../../odbc/microsoft/odbc-visual-foxpro-setup-dialog-box.md)
