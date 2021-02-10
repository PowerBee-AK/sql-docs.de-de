---
description: Bearbeiten vorhandener Datensätze
title: Bearbeiten vorhandener Datensätze | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- editing data [ADO], existing records
ms.assetid: 17ce1263-5897-452a-9ea5-c7f96b33df65
author: rothja
ms.author: jroth
ms.openlocfilehash: 031d819e2c8eed63b9b8ff42aa58fb8e998a4273
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037500"
---
# <a name="editing-existing-records"></a>Bearbeiten vorhandener Datensätze
Um vorhandene Datensätze zu bearbeiten, wechseln Sie in die Zeile, die Sie bearbeiten möchten, und ändern Sie die **value** -Eigenschaft der Felder, die Sie ändern möchten. Weitere Informationen zur **value** -Eigenschaft des **Field** -Objekts finden Sie unter unter [Suchen von Daten](./examining-data.md). Abhängig vom Cursortyp verwenden Sie **Update** oder **UpdateBatch** , um Änderungen an die Datenquelle zurückzusenden. Weitere Informationen finden Sie unter [aktualisieren und](./updating-and-persisting-data.md)beibehalten von Daten.  
  
 Es ist in der Regel effizienter, eine gespeicherte Prozedur mit einem Befehls Objekt zu verwenden, um Updates auszuführen und andere Vorgänge auszuführen, da eine gespeicherte Prozedur die Erstellung eines Cursors nicht erfordert. Weitere Informationen zu Cursorn finden Sie Untergrund Legendes zu [Cursorn und Sperren](./understanding-cursors-and-locks.md).