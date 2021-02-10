---
description: Neustrukturierung
title: Umgestaltung | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- reshaping previously shaped Recordset [ADO]
- data shaping [ADO], reshaping
ms.assetid: b1c965b7-3dad-4de6-9e0e-502ca8785be3
author: rothja
ms.author: jroth
ms.openlocfilehash: c4604bcb4713f02ffb3f804f86b429d1db3a6aab
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037080"
---
# <a name="reshaping"></a>Neustrukturierung
Einem **Recordset** , das durch eine-Klausel eines Shape-Befehls erstellt wurde, kann ein *Alias* Name zugewiesen werden (in der Regel mit dem As-Schlüsselwort). Auf den Alias eines geformten **Recordsets** kann in einem völlig anderen Befehl verwiesen werden. Das heißt, Sie können ein zuvor geformtes **Recordset** in einem neuen Shape-Befehl wieder verwenden oder *neu* strukturieren. Zur Unterstützung dieser Funktion stellt ADO eine Eigenschaft [namens "reshape](../../../ado/reference/ado-api/reshape-name-property-dynamic-ado.md)" bereit.  
  
 Die Umgestaltung verfügt über zwei Hauptfunktionen. Der erste besteht darin, ein vorhandenes **Recordset** einem neuen übergeordneten **Recordset** zuzuordnen.  
  
## <a name="example"></a>Beispiel  
  
```  
rs1.Open "SHAPE {select * from Customers} " & _  
         "APPEND ({select * from Orders} AS chapOrders " & _  
         "RELATE CustomerID to CustomerID)", cn  
  
rs2.Open "SHAPE {select * from Employees} " & _  
         "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn  
```  
  
 Die zweite Funktion besteht darin, mithilfe der Syntax "Shape" den nicht-untergeordneten **Recordset** -Zugriff auf vorhandene untergeordnete Recordsetobjekte zu aktivieren \<recordset reshape name> .  
  
> [!NOTE]
>  Es ist nicht möglich, Spalten an ein vorhandenes **Recordset** anzufügen, ein parametrisiertes **Recordset** oder die **Recordset** -Objekte in einer beliebigen dazwischenliegenden COMPUTE-Klausel neu zu strukturieren oder Aggregat Vorgänge für beliebige **Recordsets** durchzuführen, die von dem neu formatierten **Recordset** abgeleitet werden. Das **Recordset** , das umgestaltet wird, und der neue Shape-Befehl müssen beide dieselbe [Verbindung](../../../ado/reference/ado-api/connection-object-ado.md)verwenden.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Datenstrukturierung – Beispiel](../../../ado/guide/data/data-shaping-example.md)
