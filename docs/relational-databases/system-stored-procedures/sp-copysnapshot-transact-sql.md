---
description: sp_copysnapshot (Transact-SQL)
title: sp_copysnapshot (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- sp_copysnapshot
- sp_copysnapshot_TSQL
helpviewer_keywords:
- sp_copysnapshot
ms.assetid: a012a32f-6f26-45bf-8046-b51cd7fec455
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 76e8f1bead2aaf10289f724b300a79eacd3ca11f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99185776"
---
# <a name="sp_copysnapshot-transact-sql"></a>sp_copysnapshot (Transact-SQL)
[!INCLUDE [SQL Server SQL MI](../../includes/applies-to-version/sql-asdbmi.md)]

  Kopiert den Momentaufnahme Ordner der angegebenen Veröffentlichung in den Ordner, der in der **\@ destination_folder** aufgeführt ist. Diese gespeicherte Prozedur wird auf dem Verleger für die Veröffentlichungs Datenbank ausgeführt. Diese gespeicherte Prozedur ist zum Kopieren einer Momentaufnahme auf ein Wechselmedium hilfreich, wie z. B. auf eine CD-ROM.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sp_copysnapshot [ @publication = ] 'publication', [ @destination_folder = ] 'destination_folder' ]  
    [ , [ @subscriber = ] 'subscriber' ]  
    [ , [ @subscriber_db = ] 'subscriber_db' ]  
```  
  
## <a name="arguments"></a>Argumente  
`[ @publication = ] 'publication'` Der Name der Veröffentlichung, deren Momentaufnahme Inhalt kopiert werden soll. *Publication* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
`[ @destination_folder = ] 'destination_folder'` Der Name des Ordners, in den der Inhalt der Veröffentlichungs Momentaufnahme kopiert werden soll. *destination_folder* ist vom Datentyp **nvarchar (255)** und hat keinen Standardwert. Der *destination_folder* kann ein alternativer Speicherort sein, z. b. auf einem anderen Server, auf einem Netzlaufwerk oder auf einem Wechselmedium (z. b. CD-ROMs oder Wechsel Datenträgern).  
  
`[ @subscriber = ] 'subscriber'` Der Name des Abonnenten. *Subscriber* ist vom Datentyp sysname und hat den Standardwert NULL.  
  
`[ @subscriber_db = ] 'subscriber_db'` Der Name der Abonnement Datenbank. *subscriber_db* ist vom Datentyp sysname und hat den Standardwert NULL.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 **0** (Erfolg) oder **1** (Fehler)  
  
## <a name="remarks"></a>Bemerkungen  
 **sp_copysnapshot** wird bei allen Replikations Typen verwendet. Abonnenten, [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] die Version 7,0 und früher ausführen, können den alternativen Momentaufnahme Speicherort nicht verwenden.  
  
## <a name="permissions"></a>Berechtigungen  
 Nur Mitglieder der festen Server Rolle **sysadmin** oder der festen Daten Bank Rolle **db_owner** können **sp_copysnapshot** ausführen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Alternative Speicherorte für Momentaufnahme Ordner](../../relational-databases/replication/snapshot-options.md)   
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
