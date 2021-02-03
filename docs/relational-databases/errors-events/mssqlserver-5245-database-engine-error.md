---
description: MSSQLSERVER_5245
title: MSSQLSERVER_5245 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 5245 (Database Engine error)
ms.assetid: 6005c9ec-ccdd-4def-9eb4-37cdb599ddb3
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: fa96d1199c33f751dc0e49da396316b21a4f1434
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99198100"
---
# <a name="mssqlserver_5245"></a>MSSQLSERVER_5245
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|5245|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|DBCC4_TABLE_LOCK_TIMEOUT_EXCEEDED|  
|Meldungstext|Objekt-ID „O_ID“ (Objekt „NAME“): DBCC konnte keine Sperre für das Objekt erhalten, da das Timeout für die Sperranforderung überschritten wurde. Das Objekt wurde ausgelassen und wird nicht verarbeitet.|  
  
## <a name="explanation"></a>Erklärung  
Ein Sperrtimeout ist aufgetreten, während DBCC auf eine Tabellensperre für das angegebene Objekt gewartet hat.  
  
## <a name="user-action"></a>Benutzeraktion  
Führen Sie den DBCC-Befehl erneut aus.  
  
