---
description: MSSQLSERVER_41302
title: MSSQLSERVER_41302 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 41302 (Database Engine error)
ms.assetid: 01e75618-afec-4232-ba68-93ab7bc31003
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 1d01df7afff73d181cd389c417aa2283b8048f35
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99185152"
---
# <a name="mssqlserver_41302"></a>MSSQLSERVER_41302
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]|  
|Ereignis-ID|41302|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|WRITE_WRITE_CONFLICT|  
|Meldungstext|Für die aktuelle Transaktion wurde versucht, einen Datensatz zu aktualisieren, der aktualisiert wurde, nachdem diese Transaktion gestartet wurde. Die Transaktion wurde abgebrochen.|  
  
## <a name="explanation"></a>Erklärung  
Bei der Transaktion trat ein Schreibkonflikt auf und die Anweisung wurde beendet.  
  
## <a name="user-action"></a>Benutzeraktion  
Wiederholen Sie den Vorgang später in einer anderen Transaktion. Weitere Informationen finden Sie unter [In-Memory OLTP &#40;Arbeitsspeicheroptimierung&#41;](~/relational-databases/in-memory-oltp/in-memory-oltp-in-memory-optimization.md).  
  
## <a name="see-also"></a>Weitere Informationen  
[In-Memory-OLTP &#40;Arbeitsspeicheroptimierung&#41;](~/relational-databases/in-memory-oltp/in-memory-oltp-in-memory-optimization.md)  
  
