---
description: Prepared-Eigenschaft (ADO)
title: Vorbereitete Eigenschaft (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- Command15::Prepared
helpviewer_keywords:
- Prepared property [ADO]
ms.assetid: 11ca8825-765e-4bb4-a6ce-3f6564ad8755
author: rothja
ms.author: jroth
ms.openlocfilehash: e8e595f471de1219f0500f51160422ed91922e3c
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100041000"
---
# <a name="prepared-property-ado"></a>Prepared-Eigenschaft (ADO)
Gibt an, ob eine kompilierte Version eines [Befehls](./command-object-ado.md) vor der Ausführung gespeichert werden soll.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt einen **booleschen** Wert fest, der, wenn er auf **true** festgelegt ist, angibt, dass der Befehl vorbereitet werden soll, oder gibt ihn zurück.  
  
## <a name="remarks"></a>Bemerkungen  
 Verwenden Sie die **vorbereitete** Eigenschaft, damit der Anbieter eine vorbereitete (oder kompilierte) Version der Abfrage speichert, die in der [CommandText](./commandtext-property-ado.md) -Eigenschaft vor der ersten Ausführung eines [Befehls](./command-object-ado.md) Objekts angegeben ist. Dadurch kann die erste Ausführung eines Befehls verlangsamt werden. Nachdem der Anbieter jedoch einen Befehl kompiliert hat, verwendet der Anbieter die kompilierte Version des Befehls für alle nachfolgenden Ausführungen, was zu einer verbesserten Leistung führt.  
  
 Wenn die Eigenschaft auf **false** gesetzt ist, führt der Anbieter das **Befehls** Objekt direkt aus, ohne eine kompilierte Version zu erstellen.  
  
 Wenn der Anbieter die Befehls Vorbereitung nicht unterstützt, gibt er möglicherweise einen Fehler zurück, wenn diese Eigenschaft auf **true** festgelegt ist. Wenn der Anbieter keinen Fehler zurückgibt, wird die Anforderung zum Vorbereiten des Befehls einfach ignoriert und die **vorbereitete** Eigenschaft auf **false** festgelegt.  
  
## <a name="applies-to"></a>Gilt für  
 [Command-Objekt (ADO)](./command-object-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für eine vorbereitete Eigenschaft (VB)](./prepared-property-example-vb.md)   
 [Prepared-Eigenschaft – Beispiel (VC++)](./prepared-property-example-vc.md)