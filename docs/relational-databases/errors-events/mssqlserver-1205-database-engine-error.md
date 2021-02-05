---
description: MSSQLSERVER_1205
title: MSSQLSERVER_1205 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 1205 (Database Engine error)
ms.assetid: 9fe3f67c-df3c-4642-a3a4-ccc0e138b632
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 8ce9d2d99d3db0fc18586b9292876d2e4e6c985b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197167"
---
# <a name="mssqlserver_1205"></a>MSSQLSERVER_1205
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|1205|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|LK_VICTIM|  
|Meldungstext|Die Transaktion (Prozess-ID %d) befand sich auf %.*ls Ressourcen aufgrund eines anderen Prozesses in einer Deadlocksituation und wurde als Deadlockopfer ausgewählt. Führen Sie die Transaktion erneut aus.|  
  
## <a name="explanation"></a>Erklärung

Auf Ressourcen wird für separate Transaktionen in einer Reihenfolge zugegriffen, die zu einem Konflikt führt und einen [Deadlock](../sql-server-transaction-locking-and-row-versioning-guide.md?#deadlocks) verursacht. Beispiel:  
  
- Transaction1 aktualisiert **Table1.Row1** und Transaction2 aktualisiert **Table2.Row2**.
- Transaction1 versucht **Table2.Row2** zu aktualisieren. Transaction1 wird jedoch blockiert, weil für Transaction2 noch kein Commit ausgeführt wurde.  
- Nun versucht Transaction2, **Table1.Row1** zu aktualisieren. Transaction2 wird jedoch blockiert, weil für Transaction1 noch kein Commit ausgeführt wurde.
- Es kommt zu einem Deadlock, weil von Transaction1 auf die Beendigung von Transaction2 gewartet wird, während gleichzeitig von Transaction2 auf die Beendigung von Transaction1 gewartet wird.  
  
Das System erkennt diesen Deadlock und wählt eine der beteiligten Transaktionen als „Opfer“ aus. Anschließend wird diese Fehlermeldung ausgegeben, und für die Transaktion des Opfers wird ein Rollback durchgeführt.  Ausführliche Informationen finden Sie unter [Deadlocks](../sql-server-transaction-locking-and-row-versioning-guide.md?#deadlocks).

## <a name="user-action"></a>Benutzeraktion  

Führen Sie die Transaktion erneut aus. Sie können auch die Anwendung überarbeiten, um Deadlocks zu vermeiden. Die Transaktion, die als Opfer ausgewählt wurde, kann erneut ausgeführt werden und wird wahrscheinlich erfolgreich verlaufen, je nachdem, welche Vorgänge gleichzeitig ausgeführt werden.  
  
Wenn Sie Deadlocks verhindern oder vermeiden möchten, sollten alle Transaktionszugriffszeilen in derselben Reihenfolge (**Table1** und dann **Table2**) vorliegen. Auf diese Weise kann es zwar zum Blockieren kommen, ein Deadlock tritt jedoch nicht auf.  
  
Weitere Informationen finden Sie unter [Behandlung von Deadlocks](../sql-server-transaction-locking-and-row-versioning-guide.md?#handling-deadlocks) und [Minimieren von Deadlocks](../sql-server-transaction-locking-and-row-versioning-guide.md#deadlock_minimizing).
