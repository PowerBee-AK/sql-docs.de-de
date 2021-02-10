---
description: Beispiel-Recordset zum Untersuchen von Daten
title: Beispiel-Recordset zum Untersuchen von Daten | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- record location [ADO]
- current record [ADO]
ms.assetid: e770e626-68b1-4ddf-a217-d7b30311e2ee
author: rothja
ms.author: jroth
ms.openlocfilehash: baea4d79057a46ec26c6ccd82f834f5fa3481091
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037070"
---
# <a name="sample-recordset-for-examining-data"></a>Beispiel-Recordset zum Untersuchen von Daten
Betrachten wir zuerst das **Recordset** -Objekt, das mit der folgenden SQL-Abfrage zurückgegeben wird, die für die Northwind-Beispiel Datenbasis in Microsoft SQL Server ausgeführt wird.  
  
```  
SELECT ProductID,ProductName,UnitPrice   
FROM Products   
WHERE CategoryID = 7    
```  
  
 Das resultierende **Recordset** -Objekt enthält alle in der Datenbank in der folgenden Tabelle dargestellten.  
  
|ProductID|ProductName|UnitPrice|  
|---------------|-----------------|---------------|  
|7|Die organischen getrockneten Birnen von Onkel Bob|30,0000|  
|14|Dazugeben|23,2500|  
|28|Rssle-Sauerkraut|45,6000|  
|51|Von Manjimup getrocknete Äpfel|53,0000|  
|74|Longlife-Tofu|10,0000|  
  
 Wenn Sie diese Ergebnisse selbst erhalten möchten, versuchen Sie es mit dem folgenden JScript-Beispiel:  
  
-   [JScript-Beispiel für das Zurückgeben eines Recordsets](../../../ado/guide/data/jscript-code-example-to-return-a-recordset.md)
