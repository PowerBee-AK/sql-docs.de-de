---
description: MSSQLSERVER_10737
title: MSSQLSERVER_10737 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 10737 (Database Engine error)
ms.assetid: 208af6ed-b271-4ab8-803e-7666025385c8
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 05bb027048e38f976a8b32de684e59ad5cf68157
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197313"
---
# <a name="mssqlserver_10737"></a>MSSQLSERVER_10737
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|MSSQLSERVER|  
|Ereignis-ID|10737|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|REBUILD_PARTITION_ALL_NOT_SPECIFIED|  
|Meldungstext|In einer ALTER TABLE REBUILD-Anweisung oder einer ALTER INDEX REBUILD-Anweisung muss PARTITION=ALL angegeben werden, wenn in einer DATA_COMPRESSION-Klausel eine Partition angegeben ist. Mit der PARTITION=ALL-Klausel wird erzwungen, dass alle Partitionen der Tabelle oder des Indexes auch dann neu erstellt werden, wenn nur eine Teilmenge in der DATA_COMPRESSION-Klausel angegeben ist.|  
  
## <a name="user-action"></a>Benutzeraktion  
Fügen Sie die PARTITION=ALL-Klausel der ALTER TABLE-Anweisung oder der ALTER INDEX-Anweisung hinzu. Alternativ dazu können Sie REBUILD PARTITION = \<partition-number-expr> WITH (DATA_COMPRESSION={ON | OFF}) verwenden, um eine bestimmte Partition neu zu erstellen.  
  
