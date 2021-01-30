---
description: ChangePassword-Methode (ADOX)
title: ChangePassword-Methode (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _User25::raw_ChangePassword
- _User25::ChangePassword
helpviewer_keywords:
- ChangePassword method [ADOX]
ms.assetid: d187fbc6-5fac-4abb-803d-bf344dcf0302
author: rothja
ms.author: jroth
ms.openlocfilehash: 4347cb856b1fcb4d76ef6133024335404e32ad5b
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99164290"
---
# <a name="changepassword-method-adox"></a>ChangePassword-Methode (ADOX)
Ändert das Kennwort für ein [Benutzer](./user-object-adox.md) Konto.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
User.ChangePassword OldPassword, NewPassword  
```  
  
#### <a name="parameters"></a>Parameter  
 *OldPassword*  
 Ein **Zeichen** folgen Wert, der das vorhandene Kennwort des Benutzers angibt. Wenn der Benutzer zurzeit kein Kennwort hat, verwenden Sie eine leere Zeichenfolge ("") für *oldPassword*.  
  
 *NewPassword*  
 Ein **Zeichen** folgen Wert, der das neue Kennwort angibt.  
  
## <a name="remarks"></a>Bemerkungen  
 Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.  
  
 Wenn der Anbieter die Verwaltung von Vertrauens nehmer-Eigenschaften nicht unterstützt, tritt ein Fehler auf.  
  
## <a name="applies-to"></a>Gilt für  
 [User-Objekt (ADOX)](./user-object-adox.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Append- und ChangePassword-Methoden für Gruppen und Benutzer – Beispiel (VB)](./groups-and-users-append-changepassword-methods-example-vb.md)