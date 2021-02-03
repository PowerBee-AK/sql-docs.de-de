---
description: cursor (Transact-SQL)
title: cursor (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 07/23/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: reference
dev_langs:
- TSQL
helpviewer_keywords:
- cursor data type
ms.assetid: fbea16ef-f2cc-4734-9149-ec2598fd3cca
author: MikeRayMSFT
ms.author: mikeray
ms.openlocfilehash: 858a6200e1e1d74f5610d61e85a2b5dde3248e61
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205487"
---
# <a name="cursor-transact-sql"></a>cursor (Transact-SQL)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

Ein Datentyp für Variablen oder für OUTPUT-Parameter von gespeicherten Prozeduren, die einen Verweis auf einen Cursor enthalten.
  
## <a name="remarks"></a>Hinweise  
Folgende Vorgänge können auf Variablen und Parameter vom Datentyp **cursor** verweisen:
-   Die Anweisungen DECLARE *\@local_variable* und SET *\@local_variable*.  
-   Die Cursoranweisungen OPEN, FETCH, CLOSE und DEALLOCATE.  
-   Ausgabeparameter der gespeicherten Prozedur.  
-   Die CURSOR_STATUS-Funktion.  
-   Die gespeicherten Systemprozeduren **sp_cursor_list**, **sp_describe_cursor**, **sp_describe_cursor_tables** und **sp_describe_cursor_columns** .  
  
Die **cursor_name** -Ausgabespalte von **sp_cursor_list** und **sp_describe_cursor** gibt den Namen der Cursorvariablen zurück.
  
Alle Variablen, die mit dem **cursor** -Datentyp erstellt wurden, lassen NULL zu.
  
Der **cursor** -Datentyp kann nicht für eine Spalte in einer CREATE TABLE-Anweisung verwendet werden.
  
## <a name="see-also"></a>Weitere Informationen
[CAST und CONVERT &#40;Transact-SQL&#41;](../../t-sql/functions/cast-and-convert-transact-sql.md)  
[CURSOR_STATUS &#40;Transact-SQL&#41;](../../t-sql/functions/cursor-status-transact-sql.md)  
[Datentypkonvertierung &#40;Datenbank-Engine&#41;](../../t-sql/data-types/data-type-conversion-database-engine.md)  
[Datentypen &#40;Transact-SQL&#41;](../../t-sql/data-types/data-types-transact-sql.md)  
[DECLARE CURSOR &#40;Transact-SQL&#41;](../../t-sql/language-elements/declare-cursor-transact-sql.md)  
[DECLARE @local_variable &#40;Transact-SQL&#41;](../../t-sql/language-elements/declare-local-variable-transact-sql.md)  
[SET @local_variable &#40;Transact-SQL&#41;](../../t-sql/language-elements/set-local-variable-transact-sql.md)
  
  
