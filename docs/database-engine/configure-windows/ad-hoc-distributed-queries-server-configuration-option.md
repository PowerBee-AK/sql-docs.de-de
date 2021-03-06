---
title: Verteilte Ad-hoc-Abfragen (Serverkonfigurationsoption) | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie verteilte Ad-hoc-Abfragen in SQL Server aktivieren. Sie können dann OPENROWSET und OPENDATASOURCE verwenden, um eine Verbindung mit OLE DB-Remotedatenquellen herzustellen.
ms.custom: ''
ms.date: 03/02/2017
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ''
ms.technology: configuration
ms.topic: conceptual
helpviewer_keywords:
- OPENROWSET function, ad hoc distributed queries option
- Ad Hoc Distributed Queries option
- ad hoc distributed queries
- 7415 (Database Engine Error)
- OPENDATASOURCE function, ad hoc distributed queries option
- ad hoc access
ms.assetid: 5b982015-e196-44c3-83b8-275fb9d769b2
author: markingmyname
ms.author: maghan
ms.openlocfilehash: d05a89446b42feb09d46f1b407991226a7d234db
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "85698267"
---
# <a name="ad-hoc-distributed-queries-server-configuration-option"></a>Ad Hoc Distributed Queries (Serverkonfigurationsoption)
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Standardmäßig ist es in [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] nicht zulässig, dass für verteilte Ad-hoc-Abfragen OPENROWSET und OPENDATASOURCE verwendet werden. Wird diese Option auf 1 festgelegt, ist in [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] der Ad-hoc-Zugriff zulässig. Wenn diese Option nicht festgelegt oder auf 0 festgelegt wird, ist in [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] kein Ad-hoc-Zugriff zulässig.  
  
 Verteilte Ad-hoc-Abfragen verwenden die OPENROWSET- und OPENDATASOURCE-Funktionen, um eine Verbindung mit Remotedatenquellen herzustellen, die OLE DB verwenden. OPENROWSET und OPENDATASOURCE sollten nur für Verweise auf OLE DB-Datenquellen verwendet werden, auf die selten zugegriffen wird. Definieren Sie einen Verbindungsserver für Datenquellen, auf die mehr als nur wenige Male zugegriffen wird.  
  
> [!IMPORTANT]  
>  Das Aktivieren der Verwendung von Ad-hoc-Namen bedeutet, dass jede authentifizierte Anmeldung an [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] auf den Anbieter zugreifen kann. [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Administratoren sollten diese Funktion für Anbieter aktivieren, auf die von jeder lokalen Anmeldung sicher zugegriffen werden kann.  
  
## <a name="remarks"></a>Bemerkungen  
 Der Versuch, eine Ad-hoc-Verbindung ohne die Option **Ad Hoc Distributed Queries** herzustellen, verursacht den folgenden Fehler: Meldung 7415, Ebene 16, Status 1, Zeile 1  
  
 Der Ad-hoc-Zugriff auf den OLE DB-Anbieter 'Microsoft.ACE.OLEDB.12.0' wurde verweigert. Sie müssen auf diesen Anbieter über einen Verbindungsserver zugreifen.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel werden 'Ad Hoc Distributed Queries' aktiviert und anschließend ein Server mit dem Namen `Seattle1` mithilfe der `OPENROWSET` -Funktion abgefragt.  
  
```  
sp_configure 'show advanced options', 1;  
RECONFIGURE;
GO 
sp_configure 'Ad Hoc Distributed Queries', 1;  
RECONFIGURE;  
GO  
  
SELECT a.*  
FROM OPENROWSET('SQLNCLI', 'Server=Seattle1;Trusted_Connection=yes;',  
     'SELECT GroupName, Name, DepartmentID  
      FROM AdventureWorks2012.HumanResources.Department  
      ORDER BY GroupName, Name') AS a;  
GO  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Serverkonfigurationsoptionen &#40;SQL Server&#41;](../../database-engine/configure-windows/server-configuration-options-sql-server.md)   
 [Verbindungsserver &#40;Datenbank-Engine&#41;](../../relational-databases/linked-servers/linked-servers-database-engine.md)   
 [OPENROWSET &#40;Transact-SQL&#41;](../../t-sql/functions/openrowset-transact-sql.md)   
 [OPENDATASOURCE (Transact-SQL)](../../t-sql/functions/opendatasource-transact-sql.md)   
 [sp_addlinkedserver &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-addlinkedserver-transact-sql.md)  
  
  
