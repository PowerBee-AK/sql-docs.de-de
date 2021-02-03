---
description: MSSQLSERVER_3452
title: MSSQLSERVER_3452 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 3452 (Database Engine error)
ms.assetid: bf838f02-7186-4b33-b01e-361b0c02de1f
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 3e8edbc04cc3f55e867aaa4376f56b7d78715d5d
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99201583"
---
# <a name="mssqlserver_3452"></a>MSSQLSERVER_3452
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|3452|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|REC_CHECKIDENTITY|  
|Meldungstext|Bei der Wiederherstellung der '%.*ls'-Datenbank (%d) wurden mögliche inkonsistente Identitätswerte in der Tabelle mit der ID %d erkannt. Führen Sie DBCC CHECKIDENT ('%.\*ls') aus.|  
  
## <a name="explanation"></a>Erklärung  
Beim Upgrade auf [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)] wurde vom Prozess zum Wiederherstellen der Identitätswerte in der Datenbank eine Inkonsistenz in den Metadaten festgestellt.  
  
## <a name="user-action"></a>Benutzeraktion  
Führen Sie DBCC CHECKIDENT aus.  
  
