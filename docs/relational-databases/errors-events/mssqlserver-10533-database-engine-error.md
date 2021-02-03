---
description: MSSQLSERVER_10533
title: MSSQLSERVER_10533 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 10533 (Database Engine error)
ms.assetid: cc2fbdab-7b90-415f-a1f9-066824344283
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 8ef9a38232cf4613a65550a04e68f1568751547d
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197387"
---
# <a name="mssqlserver_10533"></a>MSSQLSERVER_10533
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|10533|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|PG_NAME_TOO_BIG|  
|Meldungstext|Die Planhinweisliste „%.*ls“ kann nicht erstellt werden, weil der Name der Planhinweisliste länger als die maximal zulässige Zeichenanzahl von 124 ist. Legen Sie einen Namen mit weniger als 125 Zeichen fest.|  
  
## <a name="explanation"></a>Erklärung  
Die Planhinweisliste überschreitet die maximal zulässige Zeichenanzahl von 124.  
  
## <a name="user-action"></a>Benutzeraktion  
Legen Sie einen Namen mit weniger als 125 Zeichen fest.  
  
## <a name="see-also"></a>Weitere Informationen  
[Planhinweislisten](~/relational-databases/performance/plan-guides.md)  
[sp_create_plan_guide &#40;Transact-SQL&#41;](~/relational-databases/system-stored-procedures/sp-create-plan-guide-transact-sql.md)  
[sp_create_plan_guide_from_handle &#40;Transact-SQL&#41;](~/relational-databases/system-stored-procedures/sp-create-plan-guide-from-handle-transact-sql.md)  
  
