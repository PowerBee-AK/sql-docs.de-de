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
ms.openlocfilehash: afbcf86674cf5addb8e09e1599987470660c691c
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100054095"
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