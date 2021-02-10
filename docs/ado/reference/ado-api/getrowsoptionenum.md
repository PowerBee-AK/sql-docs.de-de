---
description: GetRowsOptionEnum
title: GetRowsOptionEnum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- GetRowsOptionEnum
helpviewer_keywords:
- GetRowsOptionEnum enumeration [ADO]
ms.assetid: adc109b9-79f4-4946-a5eb-658e22e9a8a5
author: rothja
ms.author: jroth
ms.openlocfilehash: d56730ff9e9fae7a6d5a6ddc79aac8d95e17a1ca
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100020874"
---
# <a name="getrowsoptionenum"></a>GetRowsOptionEnum
Gibt an, wie viele Datensätze aus einem [Recordset](./recordset-object-ado.md)abgerufen werden sollen.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adgetrowsrest**|-1|Ruft die restlichen Datensätze im **Recordset** entweder von der aktuellen Position oder einem Lesezeichen ab, das durch den *Start* -Parameter der [GetRows](./getrows-method-ado.md) -Methode angegeben wird.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Paket: **com. ms. wfc. Data**  
  
|Konstante|  
|--------------|  
|Adoumums. getrowsoption. Rest|  
  
## <a name="applies-to"></a>Gilt für  
 [GetRows-Methode (ADO)](./getrows-method-ado.md)