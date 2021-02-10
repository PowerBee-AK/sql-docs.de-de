---
description: Flush-Methode (ADO)
title: Flush-Methode (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- _Stream::Flush
- _Stream::raw_Flush
helpviewer_keywords:
- Flush method [ADO]
ms.assetid: 938522b4-f836-4c80-8d27-a598a000f0ee
author: rothja
ms.author: jroth
ms.openlocfilehash: c4df6f318afaed7bbbc7a3302be2b1c6a15a5c1d
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100033954"
---
# <a name="flush-method-ado"></a>Flush-Methode (ADO)
Erzwingt den Inhalt des verbleibenden [Streams](./stream-object-ado.md) im ADO-Puffer für das zugrunde liegende Objekt, dem der **Stream** zugeordnet ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
Stream.Flush  
```  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Methode kann verwendet werden, um den Inhalt des Streampuffers an das zugrunde liegende Objekt zu senden, z. b. den Knoten oder die Datei, der durch die URL dargestellt wird, die die Quelle des Daten **Strom** Objekts ist. Diese Methode sollte aufgerufen werden, wenn Sie sicherstellen möchten, dass alle Änderungen, die an den Inhalten eines **Streams** vorgenommen wurden, geschrieben wurden. Allerdings ist es in der Regel nicht **erforderlich, eine Leerung aufzurufen**, da ADO den Puffer fortlaufend im Hintergrund leert. Änderungen am Inhalt eines **Streams** werden automatisch vorgenommen, nicht zwischengespeichert **, bis der** Lösch Modus aufgerufen wird.  
  
 Durch das Schließen eines **Streams** mit der [Close](./close-method-ado.md) -Methode wird der Inhalt eines **Streams** automatisch geleert. das Löschen **muss unmittelbar vor** dem **Schließen** nicht explizit aufgerufen werden.  
  
## <a name="applies-to"></a>Gilt für  
 [Stream-Objekt (ADO)](./stream-object-ado.md)