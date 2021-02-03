---
description: MSSQLSERVER_1793
title: MSSQLSERVER_1793 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
ms.assetid: 808db1d0-acc1-41d0-9287-8a5455001a02
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 44c44f6c32073bd8b93c35020dc3481867229ca8
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99196572"
---
# <a name="mssqlserver_1793"></a>MSSQLSERVER_1793
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|1793|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|FILESTREAM_BASEDATA_NEED_SAME_PARTITION|  
|Meldungstext|Das Löschen des Indexes '%.*ls' ist nicht möglich, da kein Partitionsschema für FILESTREAM-Daten angegeben wurde.|  
  
## <a name="explanation"></a>Erklärung  
Diese Meldung wird angezeigt, wenn Sie versuchen, einen gruppierten Index für eine Tabelle zu löschen, die FILESTREAM-Daten enthält, und eine **MOVE TO**-Klausel für die Basisdaten angeben, dabei aber keine **FILESTREAM_ON**-Klausel für die FILESTREAM-Daten bereitstellen.  
  
## <a name="user-action"></a>Benutzeraktion  
Verwenden Sie beim Löschen eines gruppierten Indexes in einer Tabelle, die FILESTREAM-Daten enthält, eine der folgenden Optionen:  
  
-   Geben Sie sowohl eine **MOVE TO**-Klausel für die Basisdaten als auch eine **FILESTREAM_ON**-Klausel für die FILESTREAM-Daten an.  
  
-   Geben Sie nicht entweder eine **MOVE TO**-Klausel für die Basisdaten oder eine **FILESTREAM_ON**-Klausel für die FILESTREAM-Daten an.  
  
Im folgenden Beispiel tritt ein Fehler auf, da ein Partitionsschema für die Basisdaten angegeben ist, jedoch nicht für die FILESTREAM-Daten.  
  
```Transact-SQL  
DROP INDEX [<clustered_index_name>] ON [<table_name>]   
WITH ( ONLINE = OFF, MOVE TO [PRIMARY] )  
GO  
```  
  
Das folgende Beispiel ist erfolgreich, da sowohl eine **MOVE TO**-Klausel für die Basisdaten als auch eine **FILESTREAM_ON**-Klausel für die FILESTREAM-Daten angegeben wird.  
  
```Transact-SQL  
DROP INDEX [<clustered_index_name>] ON [<table_name>]   
WITH ( ONLINE = OFF, MOVE TO [PRIMARY], filestream_on 'default' )  
GO  
```  
  
Das folgende Beispiel ist auch erfolgreich, da weder eine **MOVE TO**-Klausel für die Basisdaten noch eine **FILESTREAM_ON**-Klausel für die FILESTREAM-Daten angegeben wird.  
  
```Transact-SQL  
DROP INDEX [<clustered_index_name>] ON [<table_name>]   
WITH ( ONLINE = OFF )  
GO  
```  
  
