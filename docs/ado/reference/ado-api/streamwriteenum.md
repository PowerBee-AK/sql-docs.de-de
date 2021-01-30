---
description: StreamWriteEnum
title: Streambeschreiteenum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- StreamWriteEnum
helpviewer_keywords:
- StreamWriteEnum enumeration [ADO]
ms.assetid: bdbf3405-a0bd-4f02-85d4-e3fe8da3f3f7
author: rothja
ms.author: jroth
ms.openlocfilehash: 5be021aab95fb9fa2c0571deba176f30836a7f4e
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99170103"
---
# <a name="streamwriteenum"></a>StreamWriteEnum
Gibt an, ob ein Zeilen Trennzeichen an die Zeichenfolge angefügt wird, die in ein [Streamobjekt](./stream-object-ado.md) geschrieben wird  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adschreitechar**|0|Standard. Schreibt die angegebene Text Zeichenfolge (angegeben durch den *Daten* Parameter) in das **Stream** -Objekt.|  
|**"adschreiteline"**|1|Schreibt eine Text Zeichenfolge und ein Zeilen Trennzeichen in ein Daten **Strom** Objekt. Wenn die [lineseparser](./lineseparator-property-ado.md) -Eigenschaft nicht definiert ist, wird ein Laufzeitfehler zurückgegeben.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Diese Konstanten haben keine ADO/WFC-Entsprechungen.  
  
## <a name="applies-to"></a>Gilt für  
 [WriteText-Methode](./writetext-method.md)