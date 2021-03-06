---
description: sp_dropmergepartition (Transact-SQL)
title: sp_dropmergepartition (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
f1_keywords:
- sp_dropmergepartition_TSQL
- sp_dropmergepartition
helpviewer_keywords:
- sp_dropmergepartition
ms.assetid: 1be511c1-79ff-4947-9379-78d83b7b8945
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: c3c80582e40382d810820501515c8f11a1518f2c
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205555"
---
# <a name="sp_dropmergepartition-transact-sql"></a>sp_dropmergepartition (Transact-SQL)
[!INCLUDE [sql-asdb-asdbmi-asa-pdw](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  Entfernt eine Partition für einen parametrisierten Zeilenfilter aus einer Veröffentlichung. Diese gespeicherte Prozedur wird auf dem Verleger für die Veröffentlichungs Datenbank ausgeführt. Mit dieser gespeicherten Prozedur werden zudem der entsprechende Momentaufnahmeauftrag und die Momentaufnahmedateien für die Partition entfernt.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sp_dropmergepartition [ @publication = ] 'publication'  
        , [ @suser_sname = ] 'suser_sname'  
        , [ @host_name = ] 'host_name'  
```  
  
## <a name="arguments"></a>Argumente  
`[ @publication] = 'publication'` Der Name der Veröffentlichung. *Publication* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
`[ @suser_sname = ] 'suser_sname'` Der Wert der [SUSER_SNAME](../../t-sql/functions/suser-sname-transact-sql.md) -Funktion auf dem Abonnenten, der zum Definieren der Partition verwendet wird. *SUSER_SNAME* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
`[ @host_name = ] 'host_name'` Der Wert der [HOST_NAME](../../t-sql/functions/host-name-transact-sql.md) -Funktion auf dem Abonnenten, der zum Definieren der Partition verwendet wird. *HOST_NAME* ist vom **Datentyp vom Datentyp sysname** und hat keinen Standardwert.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 **0** (Erfolg) oder **1** (Fehler)  
  
## <a name="remarks"></a>Bemerkungen  
 **sp_dropmergepartition** wird bei der Mergereplikation verwendet.  
  
## <a name="permissions"></a>Berechtigungen  
 Nur Mitglieder der festen Server Rolle **sysadmin** oder der festen Daten Bank Rolle **db_owner** können **sp_dropmergepartition** ausführen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Verwalten von Partitionen für eine Mergeveröffentlichung mit parametrisierten Filtern](../../relational-databases/replication/publish/manage-partitions-for-a-merge-publication-with-parameterized-filters.md)  
  
  
