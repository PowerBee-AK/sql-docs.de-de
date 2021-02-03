---
description: MSSQLSERVER_3413
title: MSSQLSERVER_3413 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 3413 (Database Engine error)
ms.assetid: 3fa07637-ba93-4633-aaf2-ade7d18bc487
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 14420a895991a4ea9ed1cc7dc259ac16ad55dead
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197763"
---
# <a name="mssqlserver_3413"></a>MSSQLSERVER_3413
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|3413|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|MARKDB|  
|Meldungstext|Datenbank-ID %d. Die Datenbank konnte nicht als fehlerverdächtig gekennzeichnet werden. Fehler beim Getnext-Scan für NC für sys.databases.database_id. Identifizieren Sie die Ursache anhand vorheriger Fehlermeldungen im Fehlerprotokoll, und beheben Sie etwaige damit verbundene Probleme.|  
  
## <a name="explanation"></a>Erklärung  
Es ist ein unerwarteter Fehler aufgetreten, während versucht wurde, eine Benutzerdatenbank im Katalog als SUSPECT zu markieren. Der Status SUSPECT wird nicht beibehalten.  
  
## <a name="user-action"></a>Benutzeraktion  
Zeigen Sie vorherige Fehler an, und beheben Sie das Problem.  
  
