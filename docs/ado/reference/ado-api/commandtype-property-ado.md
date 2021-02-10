---
description: CommandType-Eigenschaft (ADO)
title: CommandType-Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Command15::CommandType
helpviewer_keywords:
- CommandType property [ADO]
ms.assetid: ca44809c-8647-48b6-a7fb-0be70a02f53e
author: rothja
ms.author: jroth
ms.openlocfilehash: 883887b32a46025c1fc60f5b8ca782241b201ab3
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100026588"
---
# <a name="commandtype-property-ado"></a>CommandType-Eigenschaft (ADO)
Gibt den Typ eines [Befehls](./command-object-ado.md) Objekts an.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen oder mehrere [CommandTypeEnum](./commandtypeenum.md) -Werte fest oder gibt ihn zurück.  
  
> [!NOTE]
>  Verwenden Sie die **commandtypeaufum** -Werte **adcmdfile** oder **adCmdTableDirect** nicht mit **CommandType**. Diese Werte können nur als Optionen mit den [Open](./open-method-ado-recordset.md) -und [Requery](./requery-method.md) -Methoden eines [Recordsets](./recordset-object-ado.md)verwendet werden.  
  
## <a name="remarks"></a>Bemerkungen  
 Verwenden Sie die **CommandType** -Eigenschaft, um die Auswertung der [CommandText](./commandtext-property-ado.md) -Eigenschaft zu optimieren.  
  
 Wenn der **CommandType** -Eigenschafts Wert auf den Standardwert **adCmdUnknown** festgelegt ist, kann die Leistung beeinträchtigt werden, da ADO Aufrufe an den Anbieter ausführen muss, um zu bestimmen, ob die **CommandText** -Eigenschaft eine SQL-Anweisung, eine gespeicherte Prozedur oder ein Tabellenname ist. Wenn Sie wissen, welche Art von Befehl Sie verwenden, weist das Festlegen der **CommandType** -Eigenschaft ADO an, direkt zum relevanten Code zu wechseln. Wenn die **CommandType** -Eigenschaft nicht mit dem Typ des Befehls in der **CommandText** -Eigenschaft identisch ist, tritt ein Fehler auf, wenn Sie die [Execute](./execute-method-ado-command.md) -Methode aufruft.  
  
## <a name="applies-to"></a>Gilt für  
 [Command-Objekt (ADO)](./command-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für ActiveConnection, CommandText, CommandTimeout, CommandType, Size und Direction Properties (VB)](./activeconnection-commandtext-commandtimeout-commandtype-size-example-vb.md)   
 [Beispiel für ActiveConnection, CommandText, CommandTimeout, CommandType, Size und Direction Properties (VC + +)](./activeconnection-commandtext-commandtimeout-commandtype-size-example-vc.md)   
 [Beispiel für ActiveConnection, CommandText, CommandTimeout, CommandType, Size und Direction Properties (JScript)](./activeconnection-commandtext-timeout-type-size-example-jscript.md)