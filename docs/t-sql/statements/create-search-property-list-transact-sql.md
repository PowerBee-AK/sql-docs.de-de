---
description: CREATE SEARCH PROPERTY LIST (Transact-SQL)
title: CREATE SEARCH PROPERTY LIST (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/10/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- CREATE_SEARCH_PROPERTY_LIST_TSQL
- CREATE SEARCH
- CREATE_SEARCH_TSQL
- CREATE_SEARCH_PROPERTY_TSQL
- CREATE SEARCH PROPERTY
- CREATE SEARCH PROPERTY LIST
- sql13.swb.spl.newsearchpropertylist.f1
dev_langs:
- TSQL
helpviewer_keywords:
- full-text search [SQL Server], search property lists
- search property lists [SQL Server], creating
- CREATE SEARCH PROPERTY LIST statement
ms.assetid: 5440cbb8-3403-4d27-a2f9-8e1f5a1bc12b
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.openlocfilehash: 31e938250b543fbb6bb3e3443138677f8ee3befd
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99192701"
---
# <a name="create-search-property-list-transact-sql"></a>CREATE SEARCH PROPERTY LIST (Transact-SQL)
[!INCLUDE [SQL Server Azure SQL Database ](../../includes/applies-to-version/sql-asdb.md)]

  Erstellt eine neue Sucheigenschaftenliste. Mit einer Sucheigenschaftenliste können eine oder mehrere Sucheigenschaften angegeben werden, die Sie in einen Volltextindex einschließen möchten.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql  
CREATE SEARCH PROPERTY LIST new_list_name  
   [ FROM [ database_name. ] source_list_name ]  
   [ AUTHORIZATION owner_name ]  
;  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="arguments"></a>Argumente
 *new_list_name*  
 Der Name der neuen Sucheigenschaftenliste. *new_list_name* ist ein Bezeichner mit maximal 128 Zeichen. *new_list_name* muss innerhalb aller Eigenschaftenlisten in der aktuellen Datenbank eindeutig sein und den Regeln für Bezeichner entsprechen. *new_list_name* wird verwendet, wenn der Volltextindex erstellt wird.  
  
 *database_name*  
 Der Name der Datenbank, in der sich die durch *source_list_name* festgelegte Eigenschaftenliste befindet. Wird *database_name* nicht angegeben, wird standardmäßig die aktuelle Datenbank verwendet.  
  
 *database_name* muss dem Namen einer vorhandenen Datenbank entsprechen. Die Anmeldung für die aktuelle Verbindung muss einer vorhandenen Benutzer-ID in der durch *database_name* festgelegte Datenbank zugeordnet sein. Sie müssen zudem über die erforderlichen [Berechtigungen](#Permissions) für die Datenbank verfügen.  
  
 *source_list_name*  
 Legt fest, dass die neue Eigenschaftenliste erstellt wird, indem eine vorhandene Eigenschaftenliste aus *database_name* kopiert wird. Wenn *source_list_name* nicht vorhanden ist, tritt bei CREATE SEARCH PROPERTY LIST ein Fehler auf. Die Sucheigenschaften in *source_list_name* werden von *new_list_name* geerbt.  
  
 AUTHORIZATION *owner_name*  
 Gibt den Namen eines Benutzers oder einer Rolle als Besitzer der Eigenschaftenliste an. *owner_name* muss der Name einer Rolle sein, deren Mitglied der aktuelle Benutzer ist, oder der aktuelle Benutzer benötigt die IMPERSONATE-Berechtigung für *owner_name*. Wird kein Wert angegeben, wird der aktuelle Benutzer zum Besitzer.  
  
> [!NOTE]  
>  Der Besitzer kann mithilfe der [ALTER AUTHORIZATION](../../t-sql/statements/alter-authorization-transact-sql.md)[!INCLUDE[tsql](../../includes/tsql-md.md)]-Anweisung geändert werden.  
  
## <a name="remarks"></a>Bemerkungen  
  
> [!NOTE]  
>  Allgemeine Informationen zu Eigenschaftenlisten finden Sie unter [Suchen von Dokumenteigenschaften mithilfe von Sucheigenschaftenlisten](../../relational-databases/search/search-document-properties-with-search-property-lists.md).  
  
 Standardmäßig sind neue Sucheigenschaftenlisten leer, und Sie müssen diesen manuell Sucheigenschaften hinzufügen. Sie können jedoch auch eine vorhandene Sucheigenschaftenliste kopieren. In diesem Fall erbt die neue Liste die Sucheigenschaften ihrer Quelle. Sie können die neue Liste jedoch ändern und Sucheigenschaften hinzufügen oder entfernen. Alle Eigenschaften, die zur Zeit der nächsten vollständigen Auffüllung in der Sucheigenschaftenliste vorhanden sind, werden in den Volltextindex aufgenommen.  
  
 Unter jeder der folgenden Bedingungen tritt bei einer CREATE SEARCH PROPERTY LIST-Anweisung ein Fehler auf:  
  
-   Die durch *database_name* festgelegte Datenbank ist nicht vorhanden.  
  
-   Die durch *source_list_name* festgelegte Liste ist nicht vorhanden.  
  
-   Wenn Sie nicht über die erforderlichen Berechtigungen verfügen.  
  
 **So fügen Sie einer Liste Eigenschaften hinzu oder entfernen sie aus einer Liste:**  
  
-   [ALTER SEARCH PROPERTY LIST &#40;Transact-SQL&#41;](../../t-sql/statements/alter-search-property-list-transact-sql.md)  
  
-   **So löschen Sie eine Eigenschaftenliste:**  
  
-   [DROP SEARCH PROPERTY LIST &#40;Transact-SQL&#41;](../../t-sql/statements/drop-search-property-list-transact-sql.md)  
  
##  <a name="permissions"></a><a name="Permissions"></a> Berechtigungen  
 Erfordert CREATE FULLTEXT CATALOG-Berechtigungen in der aktuellen Datenbank sowie REFERENCES-Berechtigungen für jede Datenbank, aus der Sie eine Quelleigenschaftenliste kopieren.  
  
> [!NOTE]  
>  Die REFERENCES-Berechtigung ist erforderlich, um die Liste einem Volltextindex zuzuordnen. Die CONTROL-Berechtigung ist erforderlich, um Eigenschaften hinzuzufügen und zu entfernen oder die Liste zu löschen. REFERENCES-Berechtigungen oder CONTROL-Berechtigungen für die Liste können vom Besitzer der Eigenschaftenliste gewährt werden. Benutzer mit CONTROL-Berechtigung können anderen Benutzern auch eine REFERENCES-Berechtigung erteilen.  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-creating-an-empty-property-list-and-associating-it-with-an-index"></a>A. Erstellen einer leeren Eigenschaftenliste und Zuordnen zu einem Index  
 Im folgenden Beispiel wird die neue Sucheigenschaftenliste `DocumentPropertyList` erstellt. Im Beispiel wird dann dem Volltextindex der `Production.Document`-Tabelle in der `AdventureWorks`-Datenbank die neue Eigenschaftenliste mithilfe einer [ALTER FULLTEXT INDEX](../../t-sql/statements/alter-fulltext-index-transact-sql.md)-Anweisung zugewiesen, ohne eine Auffüllung zu starten.  
  
> [!NOTE]  
>  Ein Beispiel, in dem dieser Sucheigenschaftenliste mehrere vordefinierte, bekannte Sucheigenschaften hinzugefügt werden, finden Sie unter [ALTER SEARCH PROPERTY LIST &#40;Transact-SQL&#41;](../../t-sql/statements/alter-search-property-list-transact-sql.md). Wenn der Liste Sucheigenschaften hinzugefügt wurden, muss der Datenbankadministrator eine weitere ALTER FULLTEXT INDEX-Anweisung mit der START FULL POPULATION-Klausel verwenden.  
  
```sql 
CREATE SEARCH PROPERTY LIST DocumentPropertyList;  
GO  
USE AdventureWorks2012;  
ALTER FULLTEXT INDEX ON Production.Document   
   SET SEARCH PROPERTY LIST DocumentPropertyList  
   WITH NO POPULATION;   
GO   
```  
  
### <a name="b-creating-a-property-list-from-an-existing-one"></a>B. Erstellen einer Eigenschaftenliste aus einer vorhandenen  
 Im folgenden Beispiel wird die neue Sucheigenschaftenliste `JobCandidateProperties` aus der in Beispiel A erstellten Liste `DocumentPropertyList` erstellt, die einem Volltextindex in der Datenbank `AdventureWorks2012` zugeordnet ist. Das Beispiel ordnet dann dem Volltextindex der `HumanResources.JobCandidate`-Tabelle in der `AdventureWorks2012`-Datenbank die neue Eigenschaftenliste mithilfe einer ALTER FULLTEXT INDEX-Anweisung zu. Mit dieser ALTER FULLTEXT INDEX-Anweisung wird eine vollständige Auffüllung gestartet, die das Standardverhalten der SET SEARCH PROPERTY LIST-Klausel darstellt.  
  
```sql  
CREATE SEARCH PROPERTY LIST JobCandidateProperties 
FROM AdventureWorks2012.DocumentPropertyList;  
GO  
ALTER FULLTEXT INDEX ON HumanResources.JobCandidate   
   SET SEARCH PROPERTY LIST JobCandidateProperties;  
GO
```  
  
## <a name="see-also"></a>Siehe auch  
 [ALTER SEARCH PROPERTY LIST &#40;Transact-SQL&#41;](../../t-sql/statements/alter-search-property-list-transact-sql.md)   
 [DROP SEARCH PROPERTY LIST &#40;Transact-SQL&#41;](../../t-sql/statements/drop-search-property-list-transact-sql.md)   
 [sys.registered_search_properties &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-registered-search-properties-transact-sql.md)   
 [sys.registered_search_property_lists &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-registered-search-property-lists-transact-sql.md)   
 [sys.dm_fts_index_keywords_by_property &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-fts-index-keywords-by-property-transact-sql.md)   
 [Suchen von Dokumenteigenschaften mithilfe von Sucheigenschaftenlisten](../../relational-databases/search/search-document-properties-with-search-property-lists.md)   
 [Suchen von Eigenschaftensatz-GUIDS und ganzzahligen Eigenschaft-IDs für Sucheigenschaften](../../relational-databases/search/find-property-set-guids-and-property-integer-ids-for-search-properties.md)  
  
  
