---
description: sp_syscollector_set_warehouse_database_name (Transact-SQL)
title: sp_syscollector_set_warehouse_database_name (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sp_syscollector_set_warehouse_database_name
- sp_syscollector_set_warehouse_database_name_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sp_syscollector_set_warehouse_database_name
- data collector [SQL Server], stored procedures
ms.assetid: a85aca1b-8135-4c81-9a05-da5aec76f1ed
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 928e72b551a976c3b51d9260248e02a4963f4052
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99159524"
---
# <a name="sp_syscollector_set_warehouse_database_name-transact-sql"></a>sp_syscollector_set_warehouse_database_name (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Gibt den in der Verbindungszeichenfolge definierten Datenbanknamen an, mit dem die Verbindung zum Verwaltungs-Data Warehouse hergestellt wird.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sp_syscollector_set_warehouse_database_name [ @database_name = ] 'database_name'  
```  
  
## <a name="arguments"></a>Argumente  
 [ @database_name =] '*database_name*'  
 Der Name des Verwaltungs Data Warehouse. *database_name* ist vom **Datentyp vom Datentyp sysname** und hat den Standardwert NULL.  
  
## <a name="return-code-values"></a>Rückgabecodewerte  
 **0** (Erfolg) oder **1** (Fehler)  
  
## <a name="remarks"></a>Bemerkungen  
 Sie müssen den Datensammler deaktivieren, bevor Sie die Konfiguration für den gesamten Datensammler ändern. Dieser Vorgang schlägt fehl, wenn der Datensammler aktiviert ist.  
  
 Um den aktuellen Datenbanknamen anzuzeigen, Fragen Sie die [syscollector_config_store](../../relational-databases/system-catalog-views/syscollector-config-store-transact-sql.md) Systemsicht ab.  
  
## <a name="permissions"></a>Berechtigungen  
 Damit diese Prozedur ausgeführt werden kann, ist die Mitgliedschaft in der festen Datenbankrolle dc_admin (mit EXECUTE-Berechtigung) erforderlich.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel wird der Name des Verwaltungs-Data Warehouse auf `RemoteMDW` festgelegt.  
  
```  
USE msdb;  
GO  
EXEC sp_syscollector_set_warehouse_database_name N'RemoteMDW';  
GO  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
