---
description: PageSize-Eigenschaft (ADO)
title: PageSize-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Recordset15::PageSize
helpviewer_keywords:
- PageSize property [ADO]
ms.assetid: e57930a6-46c4-4a17-a3b6-f79e94d5c9c7
author: rothja
ms.author: jroth
ms.openlocfilehash: 0b4e3a85d2c496f88939100a79d464bf1076fd61
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99170624"
---
# <a name="pagesize-property-ado"></a>PageSize-Eigenschaft (ADO)
Gibt an, wie viele Datensätze eine Seite im [Recordset](./recordset-object-ado.md)bilden.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen **Long** -Wert fest, der angibt, wie viele Datensätze auf einer Seite vorliegen, oder gibt ihn zurück Der Standardwert ist **10**.  
  
## <a name="remarks"></a>Bemerkungen  
 Verwenden Sie die **PageSize** -Eigenschaft, um zu bestimmen, wie viele Datensätze eine logische Datenseite bilden. Durch das Festlegen einer Seitengröße können Sie die [AbsolutePage](./absolutepage-property-ado.md) -Eigenschaft verwenden, um zum ersten Datensatz einer bestimmten Seite zu wechseln. Dies ist in Webserver Szenarios nützlich, wenn Sie es dem Benutzer ermöglichen möchten, Daten zu durchlaufen und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.  
  
 Diese Eigenschaft kann jederzeit festgelegt werden, und ihr Wert wird zum Berechnen der Position des ersten Datensatzes einer bestimmten Seite verwendet.  
  
## <a name="applies-to"></a>Gilt für  
 [Recordset-Objekt (ADO)](./recordset-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für AbsolutePage, PageCount und pageSize-Eigenschaften (VB)](./absolutepage-pagecount-and-pagesize-properties-example-vb.md)   
 [Beispiel für AbsolutePage, PageCount und pageSize-Eigenschaften (VC + +)](./absolutepage-pagecount-and-pagesize-properties-example-vc.md)   
 [AbsolutePage-Eigenschaft (ADO)](./absolutepage-property-ado.md)   
 [PageCount-Eigenschaft (ADO)](./pagecount-property-ado.md)