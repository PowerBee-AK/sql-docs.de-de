---
description: Collections (ADO/WFC-Syntax)
title: Collections (ADO-WFC-Syntax) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
helpviewer_keywords:
- syntax indexes [ADO], ADO/WFC
- collections [ADO], ADO/WFC syntax
- ADO/WFC syntax index [ADO]
ms.assetid: 073f9a0e-c755-42dd-9f71-4647d68e331a
author: rothja
ms.author: jroth
ms.openlocfilehash: f4a6ebcd488ea8f202d1383a646aa180cc5b339d
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100027088"
---
# <a name="collections-ado---wfc-syntax"></a>Collections (ADO/WFC-Syntax)
**Paket "com. ms. wfc. Data"**  
  
## <a name="parameters"></a>Parameter  
  
### <a name="methods"></a>Methoden  
  
```  
public void append(com.ms.wfc.data.Parameter param)  
public void delete(int n)  
public void delete(String s)  
public void refresh()  
public Parameter getItem(int n)  
public Parameter getItem(String s)  
```  
  
### <a name="properties"></a>Eigenschaften  
  
```  
public int getCount()  
```  
  
## <a name="fields"></a>Felder  
  
### <a name="methods"></a>Methoden  
  
```  
public void append(String name, int type)  
public void append(String name, int type, int definedSize)  
public void append(String name, int type, int definedSize, int attrib)  
public void delete(int n)  
public void delete(String s)  
public void refresh()  
public com.ms.wfc.data.Field getItem(int n)  
public com.ms.wfc.data.Field getItem(String s)  
```  
  
### <a name="properties"></a>Eigenschaften  
  
```  
public int getCount()  
```  
  
## <a name="errors"></a>Errors  
  
### <a name="methods"></a>Methoden  
  
```  
public void clear()  
public void refresh()  
public com.ms.wfc.data.Error getItem(int n)  
public com.ms.wfc.data.Error getItem(String s)  
```  
  
### <a name="properties"></a>Eigenschaften  
  
```  
public int getCount()  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Fehlersammlung (ADO)](./errors-collection-ado.md)   
 [Fields-Auflistung (ADO)](./fields-collection-ado.md)   
 [Parameters-Collection (ADO)](./parameters-collection-ado.md)