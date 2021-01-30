---
description: SetPermissions-Methode (ADOX)
title: Setberechtigungs-Methode (ADOX) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- User25::SetPermissions
- User25::raw_SetPermissions
- _Group25::SetPermissions
- _Group25::raw_SetPermissions
helpviewer_keywords:
- SetPermissions method [ADOX]
ms.assetid: b7f925d7-b05c-4376-bb49-f8d2c17b8b24
author: rothja
ms.author: jroth
ms.openlocfilehash: 3c5db51dc0af4f8e86fbaa68b20dbd82a327c038
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99164039"
---
# <a name="setpermissions-method-adox"></a>SetPermissions-Methode (ADOX)
Gibt die Berechtigungen für eine [Gruppe](./group-object-adox.md) oder einen [Benutzer](./user-object-adox.md) für ein Objekt an.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
GroupOrUser.SetPermissions Name, ObjectType, Action, Rights [, Inherit] [, ObjectTypeId]  
```  
  
#### <a name="parameters"></a>Parameter  
 *Name*  
 Ein **Zeichen** folgen Wert, der den Namen des Objekts angibt, für das Berechtigungen festgelegt werden sollen.  
  
 *ObjectType*  
 Ein **Long** -Wert, bei dem es sich um eine der [objecttypeer](./objecttypeenum.md) -Konstanten handeln kann, die den Typ des Objekts angibt, für das Berechtigungen abzurufen sind.  
  
 *Aktion*  
 Ein **Long** -Wert, der eine der [Action](./actionenum.md) Enumerationskonstanten sein kann, die den Typ der Aktion angibt, die beim Festlegen von Berechtigungen ausgeführt werden soll.  
  
 *Rechte*  
 Ein **Long** -Wert, der eine Bitmaske einer oder mehrerer [RightsEnum](./rightsenum.md) -Konstanten sein kann, die die festzulegenden Rechte angibt.  
  
 *Ver*  
 Optional. Ein **Long** -Wert, bei dem es sich [um eine der Vererbungs](./inherittypeenum.md) Konstanten handelt, die angibt, wie Objekte diese Berechtigungen erben. Der Standardwert ist " **adgeerbt None**".  
  
 *ObjectTypeId*  
 Optional. Ein **Variant** -Wert, der die GUID für einen Anbieter Objekttyp angibt, der nicht von der OLE DB Spezifikation definiert ist. Dieser Parameter ist erforderlich, wenn *ObjectType* auf **adpermubjproviderspecific** festgelegt ist. Andernfalls wird Sie nicht verwendet.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn der Anbieter das Festlegen von Zugriffsrechten für Gruppen oder Benutzer nicht unterstützt, tritt ein Fehler auf.  
  
> [!NOTE]
>  Wenn Sie **setberechtigungen** aufrufen, überschreibt das Festlegen von Aktionen auf **adaccessrevoalle** Einstellungen des *Rights* -Parameters. Legen Sie *Aktionen* nicht auf **adaccessrevofest** , wenn Sie möchten, dass die im *Rights* -Parameter angegebenen Rechte wirksam werden.  
  
## <a name="applies-to"></a>Gilt für  

:::row:::
    :::column:::
        [Group-Objekt (ADOX)](./group-object-adox.md)  
    :::column-end:::
    :::column:::
        [User-Objekt (ADOX)](./user-object-adox.md)  
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Weitere Informationen  
 [Getberechtigungs-und setberechtigungs-Methoden Beispiel (VB)](./getpermissions-and-setpermissions-methods-example-vb.md)   
 [Getberechtigungs-Methode (ADOX)](./getpermissions-method-adox.md)   
 [Name-Eigenschaft (ADOX)](./name-property-adox.md)