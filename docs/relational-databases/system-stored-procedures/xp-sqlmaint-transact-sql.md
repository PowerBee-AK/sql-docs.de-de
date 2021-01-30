---
description: xp_sqlmaint (Transact-SQL)
title: xp_sqlmaint (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- xp_sqlmaint
- xp_sqlmaint_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- xp_sqlmaint
ms.assetid: bda66e1b-6bbd-49be-b86e-37efc920e912
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 5b83e5e84d5712e9b1cf3e253222d1ef6d212720
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187949"
---
# <a name="xp_sqlmaint-transact-sql"></a>xp_sqlmaint (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Ruft das Hilfsprogramm **sqlmaint** mit einer Zeichenfolge auf, die **sqlmaint**-Schalter enthält. Das **sqlmaint** -Hilfsprogramm führt eine Reihe von Wartungs Vorgängen für eine oder mehrere Datenbanken aus.  
  
> [!NOTE]  
>  [!INCLUDE[ssNoteDepFutureAvoid](../../includes/ssnotedepfutureavoid-md.md)]  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
xp_sqlmaint 'switch_string'     
```  
  
## <a name="arguments"></a>Argumente  
 **"** *switch_string* **"**  
 Ist eine Zeichenfolge, die die **sqlmaint** -hilfsprogrammschalter enthält. Die Optionen und ihre Werte müssen durch ein Leerzeichen getrennt werden.  
  
 Der **-?** der Schalter ist für **xp_sqlmaint** ungültig.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 Keine. Gibt einen Fehler zurück, wenn das Hilfsprogramm **sqlmaint** fehlschlägt.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn diese Prozedur von einem Benutzer aufgerufen wird, der mit SQL Server-Authentifizierung angemeldet ist, werden die Schalter **-U "**_login_id_*_"_* und **"-P" für "**_Password_*_"_* vor der Ausführung *switch_string* vorangestellt. Wenn der Benutzer mit der Windows-Authentifizierung angemeldet ist, wird *switch_string* ohne Änderung an **sqlmaint** weitergegeben.  
  
## <a name="permissions"></a>Berechtigungen  
 Erfordert die Mitgliedschaft in der festen Serverrolle **sysadmin** .  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel ruft `xp_sqlmaint` das Hilfsprogramm `sqlmaint` auf, um Integritätsprüfungen auszuführen, eine Berichtsdatei zu erstellen und `msdb.dbo.sysdbmaintplan_history` zu aktualisieren.  
  
```  
EXEC xp_sqlmaint '-D AdventureWorks2012 -PlanID 02A52657-D546-11D1-9D8A-00A0C9054212   
   -Rpt "C:\Program Files\Microsoft SQL Server\MSSQL\LOG\DBMaintPlan2.txt" -WriteHistory  -CkDB -CkAl';   
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
```  
The command(s) executed successfully.  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [sqlmaint (Hilfsprogramm)](../../tools/sqlmaint-utility.md)   
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
