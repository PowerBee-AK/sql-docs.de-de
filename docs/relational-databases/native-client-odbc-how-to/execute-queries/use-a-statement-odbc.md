---
description: Verwenden einer Anweisung (ODBC)
title: Use a-Anweisung (ODBC) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: native-client
ms.topic: reference
helpviewer_keywords:
- statements [ODBC]
ms.assetid: f7573f8f-6f21-4e03-8dd5-a5f2ea4878cc
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 85b14a32b4a680da3f2a70fc18d18aca2b1ed5f3
ms.sourcegitcommit: 1a544cf4dd2720b124c3697d1e62ae7741db757c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "97473561"
---
# <a name="use-a-statement-odbc"></a>Verwenden einer Anweisung (ODBC)
[!INCLUDE [SQL Server](../../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

    
### <a name="to-use-a-statement"></a>So verwenden Sie eine Anweisung  
  
1.  Rufen Sie [SQLAllocHandle](../../../odbc/reference/syntax/sqlallochandle-function.md) mit einem *HandleType* von SQL_HANDLE_STMT auf, um ein Anweisungshandle zuzuweisen.  
  
2.  Rufen Sie optional [SQLSetStmtAttr](../../../relational-databases/native-client-odbc-api/sqlsetstmtattr.md) auf, um Anweisungsoptionen festzulegen, oder [SQLGetStmtAttr](../../../relational-databases/native-client-odbc-api/sqlgetstmtattr.md), um Anweisungsattribute abzurufen.  
  
     Um Servercursor zu verwenden, müssen Sie die Cursorattribute auf Werte setzen, die von den Standardwerten abweichen.  
  
3.  Bereiten Sie optional die Anweisung mit der [SQLPrepare-Funktion](../../../odbc/reference/syntax/sqlprepare-function.md)auf die Ausführung vor, wenn die Anweisung mehrmals ausgeführt wird.  
  
4.  Binden Sie optional mit [SQLBindParameter](../../../relational-databases/native-client-odbc-api/sqlbindparameter.md)die Parametermarkierungen an Programmvariablen, wenn die Anweisung über gebundene Parametermarkierungen verfügt. Wenn die Anweisung vorbereitet wurde, können Sie [SQLNumParams](../../../odbc/reference/syntax/sqlnumparams-function.md) und [SQLDescribeParam](../../../relational-databases/native-client-odbc-api/sqldescribeparam.md) to find the number und characteristics of the parameters.  
  
5.  Führen Sie eine Anweisung direkt mit SQLExecDirect aus.  
  
     \- oder -  
  
     Wenn die Anweisung vorbereitet wurde, führen Sie sie mehrmals mit [SQLExecute](../../../odbc/reference/syntax/sqlexecute-function.md)aus.  
  
     \- oder -  
  
     Rufen Sie eine Katalogfunktion auf, die Ergebnisse zurückgibt.  
  
6.  Verarbeiten Sie die Ergebnisse, indem Sie die Resultset-Spalten an Programmvariablen binden, indem Sie Daten mit [SQLGetData](../../../relational-databases/native-client-odbc-api/sqlgetdata.md)oder einer Kombination der beiden Methoden aus den Resultset-Spalten zu Programmvariablen verschieben.  
  
     Rufen Sie eine Zeile nach der anderen über das Resultset einer Anweisung ab.  
  
     \- oder -  
  
     Rufen Sie mehrere Zeilen gleichzeitig über das Resultset mithilfe eines Blockcursors ab.  
  
     \- oder -  
  
     Rufen Sie [SQLRowCount](../../../relational-databases/native-client-odbc-api/sqlrowcount.md) auf, um die Anzahl der Zeilen, die von einer INSERT-, UPDATE- oder DELETE-Anweisung betroffen sind, zu bestimmen.  
  
     Wenn die SQL-Anweisung über mehrere Resultsets verfügen kann, rufen Sie am Ende des Resultsets [SQLMoreResults](../../../relational-databases/native-client-odbc-api/sqlmoreresults.md) auf, um zu überprüfen, ob zusätzliche Resultsets verarbeitet werden müssen.  
  
7.  Nachdem die Ergebnisse verarbeitet wurden, müssen möglicherweise die folgenden Aktionen ausgeführt werden, um das Anweisungshandle zum Ausführen einer neuen Anweisung verfügbar zu machen.  
  
    -   Wenn Sie [SQLMoreResults](../../../relational-databases/native-client-odbc-api/sqlmoreresults.md) nicht aufgerufen haben, bis SQL_NO_DATA zurückgegeben wurde, rufen Sie [SQLCloseCursor](../../../relational-databases/native-client-odbc-api/sqlclosecursor.md) auf, um den Cursor zu schließen.  
  
    -   Wenn Sie Parametermarkierungen an Programmvariablen gebunden haben, rufen Sie [SQLFreeStmt](../../../relational-databases/native-client-odbc-api/sqlfreestmt.md) auf, wobei *Option* auf SQL_RESET_PARAMS gesetzt ist, um die gebundenen Parameter freizugeben.  
  
    -   Wenn Sie Resultset-Spalten an Programmvariablen gebunden haben, rufen Sie [SQLFreeStmt](../../../relational-databases/native-client-odbc-api/sqlfreestmt.md) auf, wobei *Option* auf SQL_UNBIND gesetzt ist, um die gebundenen Spalten freizugeben.  
  
    -   Gehen Sie zu Schritt 2, um das Anweisungshandle wiederzuverwenden.  
  
8.  Rufen Sie [SQLFreeHandle](../../../relational-databases/native-client-odbc-api/sqlfreehandle.md) mit einem *HandleType* von SQL_HANDLE_STMT auf, um das Anweisungshandle freizugeben.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Gewusst-wie-Themen zum Ausführen von Abfragen &#40;ODBC-&#41;](../../../relational-databases/native-client-odbc-how-to/execute-queries/executing-queries-how-to-topics-odbc.md)  
  
