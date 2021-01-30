---
description: SET UNIQUE-Befehl
title: Eindeutigen Befehl festlegen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- SET UNIQUE command [ODBC]
ms.assetid: 1f69e31e-4599-47cc-ac89-b86fba8703c5
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f30e589349ab1f0388e43af0aec132465b1fcdce
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99208586"
---
# <a name="set-unique-command"></a>SET UNIQUE-Befehl
Gibt an, ob Datensätze mit doppelten Index Schlüsselwerten in einer Indexdatei verwaltet werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
SET UNIQUE ON | OFF  
```  
  
## <a name="arguments"></a>Argumente  
 EIN  
 Gibt an, dass alle Datensätze mit einem doppelten Index Schlüsselwert nicht in der Indexdatei enthalten sein sollen. Nur der erste Datensatz mit dem ursprünglichen Index Schlüsselwert ist in der Indexdatei enthalten.  
  
 OFF  
 (Standard) Gibt an, dass Datensätze mit doppelten Index Schlüsselwerten in der Indexdatei enthalten sein sollen.  
  
## <a name="remarks"></a>Bemerkungen  
 Bei der Ausgabe von REINDEX wird eine Indexdatei beibehalten. Weitere Informationen finden Sie unter [Index](../../odbc/microsoft/index-command.md).
