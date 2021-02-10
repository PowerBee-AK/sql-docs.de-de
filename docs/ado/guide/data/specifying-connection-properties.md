---
description: Angeben von Verbindungseigenschaften
title: Angeben von Verbindungs Eigenschaften | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- connection properties [ADO]
- connections [ADO]
ms.assetid: 49456201-b085-4851-9686-e814136b07be
author: rothja
ms.author: jroth
ms.openlocfilehash: d69af7af414c1c864d47e39160f4b4a94d726ac9
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100032452"
---
# <a name="specifying-connection-properties"></a>Angeben von Verbindungseigenschaften
Sie können einen Großteil der durch eine [Verbindungs Zeichenfolge](../../../ado/guide/data/creating-a-connection-string.md) angegebenen Informationen bereitstellen, indem Sie die Eigenschaften des **Verbindungs** Objekts vor dem Öffnen der Verbindung festlegen. Beispielsweise können Sie denselben Effekt wie die Verbindungs Zeichenfolge erzielen, die unter [Erstellen einer Verbindungs Zeichenfolge](../../../ado/guide/data/creating-a-connection-string.md) mit dem folgenden Code erläutert wird.  
  
```  
With objConn  
.Provider = "SQLOLEDB"  
.Properties("Data Source") = "MySqlServer"  
   .Properties("Integrated Security") = "SSPI"  
.Open  
.DefaultDatabase = "Northwind"  
End With  
```  
  
 DefaultDatabase wird erst festgelegt, nachdem Sie die Verbindung geöffnet haben.  
  
> [!NOTE]
>  In ADO dürfen Sie kein Kennwort mit Semikolons (";") verwenden, es sei denn, das Kennwort ist in einfache Anführungszeichen eingeschlossen.
