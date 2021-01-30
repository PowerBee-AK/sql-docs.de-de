---
description: sp_fulltext_semantic_unregister_language_statistics_db (Transact-SQL)
title: sp_fulltext_semantic_unregister_language_statistics_db (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sp_fulltext_semantic_unregister_language_statistics_db_TSQL
- sp_fulltext_semantic_unregister_language_statistics_db
dev_langs:
- TSQL
helpviewer_keywords:
- sp_fulltext_semantic_unregister_language_statistics_db
ms.assetid: 1426ca4a-9a76-489e-98da-8f6d13ff9732
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 2d81bc4f43e93cb58b425224fb39f31a27fe7f90
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99189556"
---
# <a name="sp_fulltext_semantic_unregister_language_statistics_db-transact-sql"></a>sp_fulltext_semantic_unregister_language_statistics_db (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Hebt die Registrierung einer vorhandenen semantischen Sprachstatistikdatenbank in der aktuellen Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] auf und löscht alle zugeordneten Metadaten.  
  
 Diese Anweisung trennt die Datenbank nicht und entfernt die physische Datenbankdatei nicht aus dem Dateisystem. Nachdem Sie die Registrierung der Datenbank aufgehoben haben, können Sie sie trennen und die physische Datenbankdatei löschen.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```sql  
EXEC sp_fulltext_semantic_unregister_language_statistics_db;  
GO  
```  
  
##  <a name="arguments"></a><a name="Arguments"></a>Argumente  
 Diese Prozedur erfordert keine Argumente. Da eine Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] nur über eine semantische Sprachstatistikdatenbank verfügt, ist es nicht notwendig, die Datenbank zu identifizieren.  
  
## <a name="return-code-value"></a>Rückgabecodewert  
 **0** (Erfolg) oder **1** (Fehler)  
  
## <a name="result-set"></a>Resultset  
 Keine.  
  
## <a name="general-remarks"></a>Allgemeine Hinweise  
 Wenn die Registrierung einer semantischen Sprachstatistikdatenbank aufgehoben wird, werden auch alle zugeordneten Metadaten entfernt.  
  
 **sp_fulltext_semantic_unregister_language_statistics_db** führt die folgenden Schritte aus:  
  
1.  Überprüft, ob keine semantischen Auffüllungen für die aktuelle Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] durchgeführt werden.  
  
2.  Entfernt alle der angegebenen semantischen Sprachstatistikdatenbank zugeordneten Metadaten.  

 Weitere Informationen finden Sie unter [Installieren und Konfigurieren der semantischen Suche](../../relational-databases/search/install-and-configure-semantic-search.md).  
  
## <a name="metadata"></a>Metadaten  
 Informationen über die Semantic Language Statistics Datenbank, die auf einer Instanz von installiert [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ist, können Sie der-Katalog Sicht [sys.fulltext_semantic_language_statistics_database &#40;Transact-SQL-&#41;](../../relational-databases/system-catalog-views/sys-fulltext-semantic-language-statistics-database-transact-sql.md)Abfragen.  
  
## <a name="security"></a>Sicherheit  
  
### <a name="permissions"></a>Berechtigungen  
 Erfordert CONTROL SERVER-Berechtigungen.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel wird gezeigt, wie die Registrierung der Semantic Language Statistics-Datenbank durch Aufrufen von **sp_fulltext_semantic_unregister_language_statistics_db** aufgehoben wird.  
  
```sql  
EXEC sp_fulltext_semantic_unregister_language_statistics_db;  
GO  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Installieren und Konfigurieren der semantischen Suche](../../relational-databases/search/install-and-configure-semantic-search.md)  
  
  
