---
description: Rückgabe von SQL_NO_DATA
title: Zurückgeben SQL_NO_DATA | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SQL_NO_DATA [ODBC]
- backward compatibility [ODBC], SQL_NO_DATA
- compatibility [ODBC], SQL_NO_DATA
ms.assetid: deed0163-9d1a-4e9b-9342-3f82e64477d2
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f61d676897bf7b5633a0c9d37c12e44ae9de1cbe
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99187160"
---
# <a name="returning-sql_no_data"></a>Rückgabe von SQL_NO_DATA
Wenn eine ODBC *2. x* -Anwendung, die einen ODBC *3. x* -Treiber aufführt, **SQLExecDirect**, **SQLExecute** oder **SQLParamData** aufruft und eine gesuchte Update-oder DELETE-Anweisung ausgeführt wurde, sich jedoch nicht auf Zeilen in der Datenquelle ausgewirkt hat, sollte der ODBC *3. x* -Treiber SQL_SUCCESS zurückgeben. Wenn eine ODBC *3. x* -Anwendung, die mit einem ODBC *3. x* -Treiber arbeitet, **SQLExecDirect**, **SQLExecute** oder **SQLParamData** mit dem gleichen Ergebnis aufruft, sollte der ODBC *3. x* -Treiber SQL_NO_DATA zurückgeben.  
  
 Wenn eine gesuchte Update-oder DELETE-Anweisung in einem Batch von-Anweisungen keine Auswirkungen auf Zeilen in der Datenquelle hat, gibt **SQLMoreResults** SQL_SUCCESS zurück. Es können keine SQL_NO_DATA zurückgegeben werden, da dies bedeutet, dass keine weiteren Ergebnisse vorhanden sind, und nicht, dass ein Ergebnis aus einem durchsuchten Update/Delete vorhanden ist, das keine Zeilen betraf.
