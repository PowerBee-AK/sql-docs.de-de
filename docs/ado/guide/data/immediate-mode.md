---
title: Sofortiger Modus | Microsoft-Dokumentation
description: Beschreibt den unmittelbaren Modus, der wirksam ist, wenn die LockType-Eigenschaft auf adlockoptimierend oder adlockpessimifest gelegt ist.
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- data updates [ADO], immediate mode
- immediate mode [ADO]
- updating data [ADO], immediate mode
ms.assetid: 31fc53d0-97de-4315-a87b-3bf5cdd1f432
author: rothja
ms.author: jroth
ms.openlocfilehash: 9838a86c66abba0a73014a08a32e8e24d18849af
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037310"
---
# <a name="immediate-mode"></a>Unmittelbarer Modus
Der unmittelbare Modus ist wirksam, wenn die **LockType** -Eigenschaft auf " **adlockoptimi"** oder " **adlockpessimi"** festgelegt ist. Im unmittelbaren Modus werden Änderungen an einem Datensatz an die Datenquelle weitergegeben, sobald Sie die Arbeit in einer Zeile deklarieren, indem Sie die **Update** -Methode aufrufen.  
  
## <a name="calling-update"></a>Aufrufen von Update  
 Wenn Sie von dem Datensatz wechseln, den Sie vor dem Aufrufen der **Update** -Methode hinzufügen oder bearbeiten, wird von ADO automatisch **Update** aufgerufen, um die Änderungen zu speichern. Sie müssen die **CancelUpdate** -Methode vor der Navigation aufzurufen, wenn Sie Änderungen an dem aktuellen Datensatz abbrechen oder einen neu hinzugefügten Datensatz verwerfen möchten.  
  
 Der aktuelle Datensatz bleibt aktuell, nachdem Sie die **Update** -Methode aufgerufen haben.  
  
## <a name="cancelupdate"></a>CancelUpdate  
 Verwenden Sie die **CancelUpdate** -Methode, um Änderungen, die an der aktuellen Zeile vorgenommen wurden, abzubrechen oder eine neu hinzugefügte Zeile zu verwerfen Nachdem Sie die **Update** -Methode aufgerufen haben, können Sie keine Änderungen an der aktuellen Zeile oder einer neuen Zeile abbrechen, es sei denn, die Änderungen sind entweder Teil einer Transaktion, die Sie mit der **RollbackTrans** -Methode oder einem Teil eines Batch Updates zurücksetzen können. Im Fall eines Batch Updates können Sie das **Update** mit der **CancelUpdate** -Methode oder der **CancelBatch** -Methode abbrechen.  
  
 Wenn Sie beim aufzurufen der **CancelUpdate** -Methode eine neue Zeile hinzufügen, wird die aktuelle Zeile zur Zeile, die vor dem **AddNew** -Befehl aktuell war.  
  
 Wenn Sie die aktuelle Zeile nicht geändert oder eine neue Zeile hinzugefügt haben, generiert der Aufruf der **CancelUpdate** -Methode einen Fehler.
