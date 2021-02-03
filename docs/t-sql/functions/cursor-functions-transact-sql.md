---
description: Cursorfunktionen (Transact-SQL)
title: Cursorfunktionen (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 07/24/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
dev_langs:
- TSQL
helpviewer_keywords:
- functions [SQL Server], cursors
- cursor functions
ms.assetid: 7d9daa10-4c50-4212-9400-42120222b2b8
author: cawrites
ms.author: chadam
ms.openlocfilehash: c08ca5b485a33a31c67b2aa532c113764025a5c9
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99184086"
---
# <a name="cursor-functions-transact-sql"></a>Cursorfunktionen (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

Diese Skalarfunktionen geben Informationen über Cursor zurück:
  
- [@@CURSOR_ROWS](../../t-sql/functions/cursor-rows-transact-sql.md)
- [@@FETCH_STATUS](../../t-sql/functions/fetch-status-transact-sql.md)
- [CURSOR_STATUS](../../t-sql/functions/cursor-status-transact-sql.md)
  
Alle Cursorfunktionen sind nicht deterministisch. Das heißt, dass diese Funktionen nicht bei jeder Ausführung stets dieselben Ergebnisse zurückgeben, selbst wenn sie mit denselben Eingabewerten aufgerufen wurden. Weitere Informationen zu Funktionsdeterminismus finden Sie unter [Deterministische und nicht deterministische Funktionen](../../relational-databases/user-defined-functions/deterministic-and-nondeterministic-functions.md).
  
## <a name="see-also"></a>Weitere Informationen

[Integrierte Funktionen &#40;Transact-SQL&#41;](~/t-sql/functions/functions.md)
