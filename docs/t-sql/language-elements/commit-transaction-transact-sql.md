---
description: COMMIT TRANSACTION (Transact-SQL)
title: COMMIT TRANSACTION (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 09/09/2016
ms.prod: sql
ms.prod_service: sql-data-warehouse, database-engine, pdw, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
f1_keywords:
- COMMIT
- COMMIT TRANSACTION
- COMMIT_TSQL
- COMMIT_TRANSACTION_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- ending transactions [SQL Server]
- user-defined transactions [SQL Server]
- committed transactions
- transactions [SQL Server], ending
- marking end of transactions [SQL Server]
- implicit transactions
- distributed transactions [SQL Server], committed
- transactions [SQL Server], committed
- COMMIT TRANSACTION statement
- rolling back transactions, COMMIT TRANSACTION
ms.assetid: f8fe26a9-7911-497e-b348-4e69c7435dc1
author: cawrites
ms.author: chadam
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: b3f3997b0d5dfec86b9a12dc9645a0315e40253e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99208252"
---
# <a name="commit-transaction-transact-sql"></a>COMMIT TRANSACTION (Transact-SQL)
[!INCLUDE [sql-asdb-asdbmi-asa-pdw](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  Markiert das Ende einer erfolgreichen impliziten oder expliziten Transaktion. Ist @@TRANCOUNT gleich 1, werden von COMMIT TRANSACTION alle Datenänderungen seit dem Start der Transaktion dauerhaft in der Datenbank gespeichert. Dadurch werden die von der Transaktion belegten Ressourcen freigegeben, und @@TRANCOUNT wird auf 0 (null) herabgesetzt. Ist @@TRANCOUNT größer als 1, wird @@TRANCOUNT von COMMIT TRANSACTION lediglich um den Wert 1 verringert, und die Transaktion bleibt aktiv.  
  
 ![Artikellinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Artikellinksymbol") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
-- Applies to SQL Server (starting with 2008) and Azure SQL Database
  
COMMIT [ { TRAN | TRANSACTION }  [ transaction_name | @tran_name_variable ] ] [ WITH ( DELAYED_DURABILITY = { OFF | ON } ) ]  
[ ; ]  
```  
 
```syntaxsql
-- Applies to Azure Synapse Analytics and Parallel Data Warehouse Database
  
COMMIT [ TRAN | TRANSACTION ] 
[ ; ]  
``` 
 
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="arguments"></a>Argumente
 *transaction_name*  
 **GILT FÜR:** SQL Server und Azure SQL-Datenbank
 
 Wird vom [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] ignoriert. *transaction_name* gibt einen Transaktionsnamen an, der von einer vorherigen BEGIN TRANSACTION-Anweisung zugewiesen wurde. *transaction_name* muss den Regeln für Bezeichner entsprechen, darf jedoch 32 Zeichen nicht überschreiten. *transaction_name* zeigt den Programmierern an, welcher geschachtelten BEGIN TRANSACTION-Anweisung die COMMIT TRANSACTION-Anweisung zugeordnet ist.  
  
 *\@tran_name_variable*  
 **GILT FÜR:** SQL Server und Azure SQL-Datenbank  
 
Ist der Name einer benutzerdefinierten Variablen, die einen gültigen Transaktionsnamen enthält. Die Variable muss mit einem der folgenden Datentypen deklariert werden: char, varchar, nchar oder nvarchar. Werden mehr als 32 Zeichen an die Variable übergeben, werden nur die ersten 32 Zeichen verwendet, die restlichen Zeichen werden abgeschnitten.  
  
 DELAYED_DURABILITY  
 **GILT FÜR:** SQL Server und Azure SQL-Datenbank   

 Eine Option, die erfordert, dass für diese Transaktion ein Commit mit verzögerter Dauerhaftigkeit ausgeführt werden sollte. Die Anforderung wird ignoriert, wenn die Datenbank mit `DELAYED_DURABILITY = DISABLED` oder `DELAYED_DURABILITY = FORCED` geändert wurde. Weitere Informationen finden Sie im Thema [Steuern der Transaktionsdauerhaftigkeit](../../relational-databases/logs/control-transaction-durability.md).  
  
## <a name="remarks"></a>Bemerkungen  
 Es liegt in der Verantwortung des [!INCLUDE[tsql](../../includes/tsql-md.md)]-Programmierers, COMMIT TRANSACTION nur zu einem Zeitpunkt auszugeben, zu dem alle Daten, auf die die Transaktion verweist, logisch richtig sind.  
  
 War die Transaktion, für die ein Commit ausgeführt wird, eine verteilte [!INCLUDE[tsql](../../includes/tsql-md.md)]-Transaktion, wird MS DTC von COMMIT TRANSACTION veranlasst, mithilfe eines Zweiphasencommit-Protokolls für alle an der Transaktion beteiligten Server ein Commit auszuführen. Erstreckt sich eine lokale Transaktion über mehrere Datenbanken in derselben Instanz des [!INCLUDE[ssDE](../../includes/ssde-md.md)]s, verwendet die Instanz einen internen Zweiphasencommit, um für alle an der Transaktion beteiligten Datenbanken einen Commit auszuführen.  
  
 Bei der Verwendung in geschachtelten Transaktionen werden durch Commits der inneren Transaktionen keine Ressourcen freigegeben oder Änderungen dauerhaft gespeichert. Die Datenänderungen werden nur dann dauerhaft und Ressourcen nur dann freigegeben, wenn für die äußere Transaktion ein Commit ausgeführt wird. Bei jeder COMMIT TRANSACTION-Anweisung, die ausgegeben wird, wenn @@TRANCOUNT größer als 1 ist, wird @@TRANCOUNT einfach um 1 reduziert. Hat @@TRANCOUNT schließlich den Wert 0 (null) erreicht, wird für die gesamte äußere Transaktion ein Commit ausgeführt. Da *transaction_name* vom [!INCLUDE[ssDE](../../includes/ssde-md.md)] ignoriert wird, wird beim Ausgeben einer COMMIT TRANSACTION-Anweisung, die auf den Namen einer äußeren Transaktion verweist, @@TRANCOUNT lediglich um 1 verringert, wenn ausstehende innere Transaktionen vorhanden sind.  
  
 Hat @@TRANCOUNT den Wert 0 (null), führt die Ausgabe einer COMMIT TRANSACTION-Anweisung zu einer Fehlermeldung, da keine entsprechende BEGIN TRANSACTION-Anweisung vorhanden ist.  
  
 Nach der Ausgabe einer COMMIT TRANSACTION-Anweisung kann kein Rollback für eine Transaktion ausgeführt werden, da die Datenänderungen zu einem dauerhaften Bestandteil der Datenbank geworden sind.  
  
 Die Transaktionsanzahl in einer Anweisung wird vom [!INCLUDE[ssDE](../../includes/ssde-md.md)] nur erhöht, wenn die Transaktionsanzahl beim Start der Anweisung 0 (null) lautet.  
  
## <a name="permissions"></a>Berechtigungen  
 Erfordert die Mitgliedschaft in der **public** -Rolle.  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-committing-a-transaction"></a>A. Ausführen eines Commits für eine Transaktion  
**GILT FÜR:** SQL Server, Azure SQL-Datenbank, [!INCLUDE[ssSDW](../../includes/sssdwfull-md.md)] und [!INCLUDE[ssPDW](../../includes/sspdw-md.md)]   

Im folgenden Beispiel wird ein Stellenbewerber gelöscht. AdventureWorks wird verwendet. 
  
```sql   
BEGIN TRANSACTION;   
DELETE FROM HumanResources.JobCandidate  
    WHERE JobCandidateID = 13;   
COMMIT TRANSACTION;   
```  
  
### <a name="b-committing-a-nested-transaction"></a>B. Ausführen eines Commits für eine geschachtelte Transaktion  
**GILT FÜR:** SQL Server und Azure SQL-Datenbank    

Im folgenden Beispiel werden eine Tabelle erstellt und drei Ebenen von geschachtelten Transaktionen generiert, und anschließend wird für die geschachtelte Transaktion ein Commit ausgeführt. Obwohl jede `COMMIT TRANSACTION`-Anweisung einen *transaction_name*-Parameter aufweist, gibt es keine Beziehung zwischen der `COMMIT TRANSACTION`-Anweisung und der `BEGIN TRANSACTION`-Anweisung. Die *transaction_name*-Parameter helfen dem Programmierer, die richtige Anzahl von Commits zu codieren, damit `@@TRANCOUNT` auf 0 (null) herabgesetzt und dadurch für die äußere Transaktion ein Commit ausgeführt wird. 
  
```sql   
IF OBJECT_ID(N'TestTran',N'U') IS NOT NULL  
    DROP TABLE TestTran;  
GO  
CREATE TABLE TestTran (Cola INT PRIMARY KEY, Colb CHAR(3));  
GO  
-- This statement sets @@TRANCOUNT to 1.  
BEGIN TRANSACTION OuterTran;  
  
PRINT N'Transaction count after BEGIN OuterTran = '  
    + CAST(@@TRANCOUNT AS NVARCHAR(10));  
 
INSERT INTO TestTran VALUES (1, 'aaa');  
 
-- This statement sets @@TRANCOUNT to 2.  
BEGIN TRANSACTION Inner1;  
 
PRINT N'Transaction count after BEGIN Inner1 = '  
    + CAST(@@TRANCOUNT AS NVARCHAR(10));  
  
INSERT INTO TestTran VALUES (2, 'bbb');  
  
-- This statement sets @@TRANCOUNT to 3.  
BEGIN TRANSACTION Inner2;  
  
PRINT N'Transaction count after BEGIN Inner2 = '  
    + CAST(@@TRANCOUNT AS NVARCHAR(10));  
  
INSERT INTO TestTran VALUES (3, 'ccc');  
  
-- This statement decrements @@TRANCOUNT to 2.  
-- Nothing is committed.  
COMMIT TRANSACTION Inner2;  
 
PRINT N'Transaction count after COMMIT Inner2 = '  
    + CAST(@@TRANCOUNT AS NVARCHAR(10));  
 
-- This statement decrements @@TRANCOUNT to 1.  
-- Nothing is committed.  
COMMIT TRANSACTION Inner1;  
 
PRINT N'Transaction count after COMMIT Inner1 = '  
    + CAST(@@TRANCOUNT AS NVARCHAR(10));  
  
-- This statement decrements @@TRANCOUNT to 0 and  
-- commits outer transaction OuterTran.  
COMMIT TRANSACTION OuterTran;  
  
PRINT N'Transaction count after COMMIT OuterTran = '  
    + CAST(@@TRANCOUNT AS NVARCHAR(10));  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [BEGIN DISTRIBUTED TRANSACTION &#40;Transact-SQL&#41;](../../t-sql/language-elements/begin-distributed-transaction-transact-sql.md)   
 [BEGIN TRANSACTION &#40;Transact-SQL&#41;](../../t-sql/language-elements/begin-transaction-transact-sql.md)   
 [COMMIT WORK &#40;Transact-SQL&#41;](../../t-sql/language-elements/commit-work-transact-sql.md)   
 [ROLLBACK TRANSACTION &#40;Transact-SQL&#41;](../../t-sql/language-elements/rollback-transaction-transact-sql.md)   
 [ROLLBACK WORK &#40;Transact-SQL&#41;](../../t-sql/language-elements/rollback-work-transact-sql.md)   
 [SAVE TRANSACTION &#40;Transact-SQL&#41;](../../t-sql/language-elements/save-transaction-transact-sql.md)   
 [@@TRANCOUNT &#40;Transact-SQL&#41;](../../t-sql/functions/trancount-transact-sql.md)  
  
