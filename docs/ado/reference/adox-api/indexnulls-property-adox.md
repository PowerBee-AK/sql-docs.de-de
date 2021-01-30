---
description: IndexNulls-Eigenschaft (ADOX)
title: IndexNulls-Eigenschaft (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Index::get_IndexNulls
- _Index::GetIndexNulls
- _Index::put_IndexNulls
- _Index::PutIndexNulls
- _Index::IndexNulls
helpviewer_keywords:
- IndexNulls property [ADOX]
ms.assetid: 313b0bf7-3f37-4823-8fca-bd9c80e078a7
author: rothja
ms.author: jroth
ms.openlocfilehash: bf41734c44e4ae2347cdaf560167b72003716f7f
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99169353"
---
# <a name="indexnulls-property-adox"></a>IndexNulls-Eigenschaft (ADOX)
Gibt an, ob Datensätze mit NULL-Werten in ihren Indexfeldern Indexeinträge aufweisen.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen [AllowNullsEnum](./allownullsenum.md) -Wert fest und gibt ihn zurück. Der Standardwert ist **adIndexNullsDisallow**.  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Eigenschaft ist für [Index](./index-object-adox.md) Objekte, die bereits an eine Auflistung angehängt wurden, schreibgeschützt.  
  
## <a name="applies-to"></a>Gilt für  
 [Index-Objekt (ADOX)](./index-object-adox.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [IndexNulls-Eigenschaft – Beispiel (VB)](./indexnulls-property-example-vb.md)