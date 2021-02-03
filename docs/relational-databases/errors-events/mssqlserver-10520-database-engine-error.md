---
description: MSSQLSERVER_10520
title: MSSQLSERVER_10520 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 10520 (Database Engine error)
ms.assetid: cc8799f1-5b90-4248-b209-e1d5087f9529
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 0f2187ccd80b90c0375ae960bd4e27806640e74b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197447"
---
# <a name="mssqlserver_10520"></a>MSSQLSERVER_10520
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|10520|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|PG_PARAM_NOT_ALLOWED|  
|Meldungstext|Die Planhinweisliste „%.*ls“ kann nicht erstellt werden, weil @type als „%ls“ angegeben und ein Wert ungleich NULL für den „%ls“-Parameter festgelegt wurde. Dieser Typ erfordert einen NULL-Wert für den Parameter. Geben Sie NULL für den Parameter an, oder ändern Sie den Typ in einen Typ, der Werte ungleich NULL für den Parameter zulässt.|  
  
## <a name="explanation"></a>Erklärung  
Der in @type angegebene Typ erfordert einen Wert NULL für den angegebenen Parameter. Es wurde jedoch ein Wert ungleich NULL angegeben.  
  
## <a name="user-action"></a>Benutzeraktion  
Geben Sie NULL für den Parameter an, oder ändern Sie den Typ in einen Typ, der Werte ungleich NULL für den Parameter zulässt.  
  
## <a name="see-also"></a>Weitere Informationen  
[sp_create_plan_guide &#40;Transact-SQL&#41;](~/relational-databases/system-stored-procedures/sp-create-plan-guide-transact-sql.md)  
[Planhinweislisten](~/relational-databases/performance/plan-guides.md)  
  
