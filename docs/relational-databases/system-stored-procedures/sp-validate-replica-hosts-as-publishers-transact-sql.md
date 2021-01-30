---
title: sp_validate_replica_hosts_as_publishers (T-SQL)
description: Beschreibt die gespeicherte Prozedur sp_validate_replica_hosts_as_publishers, mit der alle sekundären Replikate überprüft werden können.
ms.custom: seo-lt-2019
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- sp_validate_replica_hosts_as_publishers_TSQL
- sp_validate_replica_hosts_as_publishers
helpviewer_keywords:
- sp_validate_replica_hosts_as_publishers
ms.assetid: 45001fc9-2dbd-463c-af1d-aa8982d8c813
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 4f00ca4f972b7fccfa09f9c36c8e5b7fa09420fd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205513"
---
# <a name="sp_validate_replica_hosts_as_publishers-transact-sql"></a>sp_validate_replica_hosts_as_publishers (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  **sp_validate_replica_hosts_as_publishers** ist eine Erweiterung von **sp_validate_redirected_publisher** , mit der alle sekundären Replikate überprüft werden können, und nicht nur das aktuelle primäre Replikat. **sp_validate_replicat_hosts_as_publisher** überprüft eine gesamte Always on Replikations Topologie. **sp_validate_replica_hosts_as_publishers** muss direkt auf dem Verteiler ausgeführt werden, indem eine Remote Desktop Sitzung verwendet wird, um einen Double-Hop-Sicherheitsfehler (21892) zu vermeiden.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sp_validate_replica_hosts_as_publishers   
    [ @original_publisher = ] 'original_publisher',  
    [ @publisher_db = ] 'database_name',   
    [ @redirected_publisher = ] 'new_publisher' output  
```  
  
## <a name="arguments"></a>Argumente  
`[ @original_publisher = ] 'original_publisher'` Der Name der Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] , die die Datenbank ursprünglich veröffentlicht hat. *original_publisher* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
`[ @publisher_db = ] 'publisher_db'` Der Name der Datenbank, die veröffentlicht wird. *publisher_db* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
`[ @redirected_publisher = ] 'redirected_publisher'` Das Ziel der Umleitung, wenn **sp_redirect_publisher** für das ursprüngliche Verleger-/Veröffentlichungs-Datenbankpaar aufgerufen wurde. *redirected_publisher* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 **0** (Erfolg) oder **1** (Fehler)  
  
## <a name="result-sets"></a>Resultsets  
 Keine.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn kein Eintrag für den Verleger und die Veröffentlichungs Datenbank vorhanden ist, gibt **sp_validate_redirected_publisher** für den *\@ redirected_publisher* Output-Parameter den Wert NULL zurück. Andernfalls wird der zugeordnete umgeleitete Verleger zurückgegeben, sowohl bei Erfolg und als auch bei Fehler.  
  
 Wenn die Überprüfung erfolgreich ist, gibt **sp_validate_redirected_publisher** eine Erfolgs Angabe zurück.  
  
 Wenn die Überprüfung fehlschlägt, werden entsprechende Fehler ausgelöst.  **sp_validate_redirected_publisher** hat den besten Aufwand, alle Probleme und nicht nur das erste gefundene Problem zu beheben.  
  
> [!NOTE]  
>  **sp_validate_replica_hosts_as_publishers** schlägt bei der Überprüfung sekundärer Replikathosts, die keinen Lesezugriff zulassen oder die Angabe der Leseabsicht erfordern, mit dem folgenden Fehler fehl.  
>   
>  Meldung 21899, Ebene 11, Status 1, Prozedur **sp_hadr_verify_subscribers_at_publisher**, Zeile 109  
>   
>  Die Abfrage beim umgeleiteten Verleger „MyReplicaHostName“ zur Bestimmung, ob sysserver-Einträge für die Abonnenten des ursprünglichen Verlegers „MyOriginalPublisher“ vorliegen, ist mit Fehler 976 und folgender Meldung fehlgeschlagen: „Fehler 976, Stufe 14, Status 1, Meldung: The target database, 'MyPublishedDB', is participating in an availability group and is currently not accessible for queries. (Die Zieldatenbank „MyPublishedDB“ ist an einer Verfügbarkeitsgruppe beteiligt, und Abfragen können derzeit nicht darauf zugreifen.) Entweder die Datenverschiebung wurde angehalten, oder für das Verfügbarkeitsreplikat wurde kein Schreibzugriff aktiviert. Um schreibgeschützten Zugriff auf diese und andere Datenbanken in der Verfügbarkeitsgruppe zuzulassen, aktivieren Sie den Lesezugriff auf mindestens ein sekundäres Verfügbarkeitsreplikat in der Gruppe.  Weitere Informationen finden Sie in der **ALTER AVAILABILITY GROUP** -Anweisung in der [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Onlinedokumentation.  
>   
>  Es sind ein oder mehrere Verlegerüberprüfungsfehler für Replikathost 'MyReplicaHostName' aufgetreten.  
  
## <a name="permissions"></a>Berechtigungen  
 Der Aufrufer muss entweder ein Mitglied der festen Server Rolle **sysadmin** , der festen Daten Bank Rolle **db_owner** für die Verteilungs Datenbank oder ein Mitglied einer Veröffentlichungs Zugriffsliste für eine der Verleger Datenbank zugeordnete definierte Veröffentlichung sein.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Gespeicherte Replikationsprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/replication-stored-procedures-transact-sql.md)   
 [sp_get_redirected_publisher &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-get-redirected-publisher-transact-sql.md)   
 [sp_redirect_publisher &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-redirect-publisher-transact-sql.md)   
 [sp_validate_redirected_publisher &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-validate-redirected-publisher-transact-sql.md)  
  
  
