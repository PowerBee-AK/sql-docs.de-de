---
description: StringFormatEnum
title: Stringformatumum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- StringFormatEnum
helpviewer_keywords:
- StringFormatEnum enumeration [ADO]
ms.assetid: 28f7d1ec-092b-4323-a39d-d3f882c6c81a
author: rothja
ms.author: jroth
ms.openlocfilehash: b23a6bc4354f4c67c07bcdc1f4b4d463fff072f2
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100056505"
---
# <a name="stringformatenum"></a>StringFormatEnum
Gibt das Format beim Abrufen eines [Recordsets](./recordset-object-ado.md) als Zeichenfolge an.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adclipstring**|2|Begrenzt Zeilen nach *RowDelimiter*, Spalten nach *ColumnDelimiter* und NULL-Werte durch *nullexpr*. Diese drei Parameter der [GetString](./getstring-method-ado.md) -Methode sind nur mit einem *StringFormat* von **adclipstring** gültig.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|AdoEnums. StringFormat. clipstring|  
  
## <a name="applies-to"></a>Gilt für  
 [GetString-Methode (ADO)](./getstring-method-ado.md)