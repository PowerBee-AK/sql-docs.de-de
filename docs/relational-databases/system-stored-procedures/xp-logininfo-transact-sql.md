---
description: xp_logininfo (Transact-SQL)
title: xp_logininfo (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- xp_logininfo_TSQL
- xp_logininfo
dev_langs:
- TSQL
helpviewer_keywords:
- xp_logininfo
ms.assetid: ee7162b5-e11f-4a0e-a09c-1878814dbbbd
author: VanMSFT
ms.author: vanto
ms.openlocfilehash: 6df69edd25c5c2f451e8a4aa657caf99a4c8103d
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99124101"
---
# <a name="xp_logininfo-transact-sql"></a>xp_logininfo (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Gibt Informationen zu Windows-Benutzern und Windows-Gruppen zurück.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
xp_logininfo [ [ @acctname = ] 'account_name' ]   
     [ , [ @option = ] 'all' | 'members' ]   
     [ , [ @privilege = ] variable_name OUTPUT]  
```  
  
## <a name="arguments"></a>Argumente  
`[ @acctname = ] 'account_name'` Der Name eines Windows-Benutzers oder einer Windows-Gruppe, dem der Zugriff gewährt wird [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] . *account_name* ist vom Datentyp **sysname** und hat den Standardwert NULL. Wenn *account_name* nicht angegeben wird, werden alle Windows-Gruppen und Windows-Benutzer ausgegeben, denen explizit Anmeldeberechtigungen gewährt wurden. *account_name* muss vollqualifiziert sein. Beispiel: 'ADVWKS4\macraes' oder 'VORDEFINIERT\Administratoren'.  
  
 **"alle"**  |  **' Members '**  
 Gibt an, ob für das Konto die Informationen zu allen Berechtigungspfaden oder nur die Informationen zu den Mitgliedern der Windows-Gruppe ausgegeben werden sollen. die **\@ Option** ist vom Datentyp **varchar (10)** und hat den Standardwert NULL. Sofern nicht **all** angegeben wurde, wird nur der erste Berechtigungspfad angezeigt.  
  
`[ @privilege = ] variable_name` Ist ein Ausgabeparameter, der die Berechtigungsstufe des angegebenen Windows-Kontos zurückgibt. *variable_name* ist vom Datentyp **varchar(10)**. Der Standardwert ist "Not wanted". Die zurückgegebene Privilegstufe ist **user**, **admin** oder **null**.  
  
 OUTPUT  
 Wenn dieser Parameter angegeben wird, wird *variable_name* in den Ausgabeparameter platziert.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 „0“ (erfolgreich) oder „1“ (fehlerhaft)  
  
## <a name="result-sets"></a>Resultsets  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**Kontoname**|**sysname**|Der vollqualifizierte Windows-Kontoname.|  
|**type**|**char (8)**|Der Windows-Kontotyp. Gültige Werte sind **user** oder **group**.|  
|**Ehre**|**char(9)**|Das Zugriffsprivileg für [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Gültige Werte sind **admin**, **user** oder **null**.|  
|**mapped login name**|**sysname**|Für Benutzerkonten mit Benutzerprivileg wird mit **mapped login name** der zugeordnete Anmeldename angezeigt, den [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] bei der Anmeldung mit diesem Konto zu verwenden versucht. Dabei werden die Zuordnungsregeln mit Voranstellung des Domänennamens verwendet.|  
|**permission path**|**sysname**|Die Gruppenmitgliedschaft, die dem Konto den Zugriff ermöglicht hat.|  
  
## <a name="remarks"></a>Bemerkungen  
 Wird *account_name* angegeben, meldet **xp_logininfo** die höchste Privilegstufe des angegebenen Windows-Benutzers bzw. der angegebenen Windows-Gruppe. Wenn ein Windows-Benutzer Zugriff als Systemadministrator und als Domänenbenutzer hat, wird er nur als Systemadministrator gemeldet. Gehört der Benutzer mehreren Windows-Gruppen derselben Privilegstufe an, wird nur die Gruppe gemeldet, der zuerst Zugriff auf [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] erteilt wurde.  
  
 Wenn *account_name* ein gültiger Windows-Benutzer oder eine gültige Windows-Gruppe ist, dem bzw. der kein [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Anmeldename zugeordnet ist, wird ein leeres Resultset zurückgegeben. Wenn *account_name* nicht als gültiger Windows-Benutzer oder als gültige Windows-Gruppe identifiziert werden kann, wird ein Fehler gemeldet.  
  
 Werden *account_name* und **all** angegeben, werden sämtliche Berechtigungspfade für den Windows-Benutzer oder die Windows-Gruppe zurückgegeben. Wenn *account_name* mehreren Gruppen angehört, denen allen Zugriff auf [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]erteilt wurde, werden mehrere Zeilen zurückgegeben. Die Zeilen für das **admin** -Privileg werden vor den Zeilen für das **user** -Privileg zurückgegeben. Innerhalb einer Privilegstufe werden die Zeilen in der Reihenfolge zurückgegeben, in der die entsprechenden [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Anmeldenamen erstellt wurden.  
  
 Wenn *account_name* und **members** angegeben werden, wird eine Liste der Gruppenmitglieder der nächsten Ebene zurückgegeben. Ist *account_name* der Name einer lokalen Gruppe, kann die Liste lokale Benutzer, Domänenbenutzer und Gruppen enthalten. Wenn *account_name* ein Domänenkonto ist, besteht die Liste aus Domänenbenutzern. [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] muss eine Verbindung mit dem Domänencontroller herstellen, um Informationen zu Gruppenmitgliedschaften abzurufen. Falls der Server keine Verbindung mit dem Domänencontroller herstellen kann, werden keine Informationen zurückgegeben.  
  
 **xp_logininfo** gibt nur Informationen von Active Directory globalen Gruppen zurück, nicht für universelle Gruppen.  
  
## <a name="permissions"></a>Berechtigungen  
 Mitgliedschaft in der festen Serverrolle **sysadmin** bzw. Mitgliedschaft in der festen Datenbankrolle **public** in der **master** -Datenbank mit erteilter EXECUTE-Berechtigung erforderlich.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel werden Informationen zur Windows-Gruppe `BUILTIN\Administrators` angezeigt.  
  
```  
EXEC xp_logininfo 'BUILTIN\Administrators';  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [sp_denylogin &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-denylogin-transact-sql.md)   
 [sp_grantlogin &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-grantlogin-transact-sql.md)   
 [sp_revokelogin &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-revokelogin-transact-sql.md)   
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)   
 [Allgemeine erweiterte gespeicherte Prozeduren &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/general-extended-stored-procedures-transact-sql.md)  
  
  
