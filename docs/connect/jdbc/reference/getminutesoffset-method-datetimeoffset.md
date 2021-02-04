---
description: getMinutesOffset-Methode (DateTimeOffset)
title: getMinutesOffset-Methode (DateTimeOffset) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: 18ba844a-ea36-42de-87da-bbc222082efe
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 44fe6c4be49cc8896ee1f59e3794617e839d8744
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99175463"
---
# <a name="getminutesoffset-method-datetimeoffset"></a>getMinutesOffset-Methode (DateTimeOffset)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Gibt die Abweichung dieses DateTimeOffset-Objekts von GMT in Minuten zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
public int getMinutesOffset()  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Das Offset in Minuten.  
  
## <a name="remarks"></a>Bemerkungen  
 Für ein DateTimeOffset-Objekt, das den 8. März 2010 11:35:48 -0800 darstellt, gibt getMinutesOffset den Wert „480“ zurück.  
  
## <a name="see-also"></a>Weitere Informationen  
 [DateTimeOffset-Klasse](../../../connect/jdbc/reference/datetimeoffset-class.md)   
 [DateTimeOffset-Elemente](../../../connect/jdbc/reference/datetimeoffset-members.md)  
  
  
