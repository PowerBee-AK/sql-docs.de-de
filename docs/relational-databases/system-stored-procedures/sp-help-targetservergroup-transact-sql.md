---
description: sp_help_targetservergroup (Transact-SQL)
title: sp_help_targetservergroup (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 08/09/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sp_help_targetservergroup_TSQL
- sp_help_targetservergroup
dev_langs:
- TSQL
helpviewer_keywords:
- sp_help_targetservergroup
ms.assetid: ec3a4a68-b591-431c-9518-053ede522d0c
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 200b6b0a8d6a6700f7aa98db0cde45cfc278dc53
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99186700"
---
# <a name="sp_help_targetservergroup-transact-sql"></a>sp_help_targetservergroup (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Listet alle Zielserver in der angegebenen Gruppe auf. Wenn keine Gruppe angegeben wird, gibt [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Informationen zu allen Zielservergruppen zurück.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sp_help_targetservergroup  
    [ [ @name = ] 'name' ]  
```  
  
## <a name="argument"></a>Argument  
`[ @name = ] 'name'` Der Name der Zielserver Gruppe, für die Informationen zurückgegeben werden sollen. *name* ist vom Datentyp **sysname** und hat den Standardwert NULL.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 **0** (Erfolg) oder **1** (Fehler)  
  
## <a name="result-sets"></a>Resultsets  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**servergroup_id**|**int**|ID der Servergruppe.|  
|**name**|**sysname**|Name der Servergruppe.|  
  
## <a name="permissions"></a>Berechtigungen  
 Die Berechtigungen zum Ausführen dieser Prozedur werden standardmäßig der festen Server Rolle **sysadmin** zugewiesen.  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-listing-information-for-all-target-server-groups"></a>A. Auflisten von Informationen für alle Zielservergruppen  
 In diesem Beispiel werden Informationen für alle Zielservergruppen aufgelistet.  
  
```  
USE msdb ;  
GO  
  
EXEC dbo.sp_help_targetservergroup ;  
GO  
```  
  
### <a name="b-listing-information-for-a-specific-target-server-group"></a>B. Auflisten von Informationen für eine bestimmte Zielservergruppe  
 In diesem Beispiel werden Informationen für die `Servers Maintaining Customer Information`-Zielservergruppe aufgelistet.  
  
```  
USE msdb ;  
GO  
  
EXEC dbo.sp_help_targetservergroup   
    N'Servers Maintaining Customer Information' ;  
GO  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [sp_add_targetservergroup &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-add-targetservergroup-transact-sql.md)   
 [sp_delete_targetservergroup &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-delete-targetservergroup-transact-sql.md)   
 [sp_update_targetservergroup &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-update-targetservergroup-transact-sql.md)   
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
