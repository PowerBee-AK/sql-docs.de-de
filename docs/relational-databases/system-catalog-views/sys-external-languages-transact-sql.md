---
description: sys.external_languages (Transact-SQL)-SQL Server
title: sys.external_languages (Transact-SQL)-SQL Server | Microsoft-Dokumentation
ms.custom: ''
ms.date: 05/22/2019
ms.prod: sql
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- external_languages
- external_languages_TSQL
- sys.external_languages
- sys.external_languages_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.external_languages catalog view
author: nelgson
ms.author: negust
ms.reviewer: dphansen
manager: cgronlun
monikerRange: '>=sql-server-ver15'
ms.openlocfilehash: d0532579a372c264bf2477026d56275431610bf3
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99193930"
---
# <a name="sysexternal_languages-transact-sql"></a>sys.external_languages (Transact-SQL)
[!INCLUDE[SQL Server 2019](../../includes/applies-to-version/sqlserver2019.md)]

Diese Katalog Sicht enthält eine Liste der externen Sprachen in der Datenbank. **R** und **Python** sind reservierte Namen, und es kann keine externe Sprache mit diesen Namen erstellt werden.

## <a name="sysexternal_languages"></a>sys.external_languages

Die Katalog Sicht sys.external_languages listet eine Zeile für jede externe Sprache in der Datenbank auf.

|Spaltenname |Datentyp | BESCHREIBUNG|
|------|------|------|
|external_language_id |INT | ID der externen Sprache|
|language |sysname |Der Name der externen Sprache. Ist in der Datenbank eindeutig. R und python sind reservierte Namen pro Instanz.|
|create_date |datetime2 |Datum und Uhrzeit der Erstellung|
|principal_id |INT |ID des Prinzipals, der diese externe Bibliothek besitzt.|

## <a name="see-also"></a>Siehe auch  

+ [sys.external_language_files](sys-external-language-files-transact-sql.md)  
+ [externe Sprache erstellen](../../t-sql/statements/create-external-language-transact-sql.md) 
