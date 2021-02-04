---
description: sqlsrv_get_config
title: sqlsrv_get_config | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- sqlsrv_get_config
apitype: NA
helpviewer_keywords:
- API Reference, sqlsrv_get_config
- sqlsrv_get_config
ms.assetid: ce2befc2-af98-45bb-8d41-60f1674dccfc
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: a59f7be566ab349ae6edd3eabf6ed99c32dc707f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99154107"
---
# <a name="sqlsrv_get_config"></a>sqlsrv_get_config
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

Gibt den aktuellen Wert der angegebenen Konfigurationseinstellung zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sqlsrv_get_config( string $setting )  
```  
  
#### <a name="parameters"></a>Parameter  
*$setting*: Die Konfigurationseinstellung für die der Wert zurückgegeben wird. Eine Liste der konfigurierbaren Einstellungen finden Sie unter [sqlsrv_configure](../../connect/php/sqlsrv-configure.md).  
  
## <a name="return-value"></a>Rückgabewert  
Der Wert der Einstellung, angegeben durch den *$setting* -Parameter. Wenn eine ungültige Einstellung angegeben wird, wird **false** zurückgegeben und ein Fehler wird zur Fehlersammlung hinzugefügt.  
  
## <a name="remarks"></a>Hinweise  
Wenn **false** von **sqlsrv_get_config** zurückgegeben wird, müssen Sie [sqlsrv_errors](../../connect/php/sqlsrv-errors.md) aufrufen, um zu bestimmen, ob ein Fehler aufgetreten ist oder ob **false** der Wert der durch den *$setting* -Parameter.  
  
## <a name="see-also"></a>Weitere Informationen  
[API-Referenz für den SQLSRV-Treiber](../../connect/php/sqlsrv-driver-api-reference.md)  

[sqlsrv_configure](../../connect/php/sqlsrv-configure.md)  

[sqlsrv_errors](../../connect/php/sqlsrv-errors.md)  
  
