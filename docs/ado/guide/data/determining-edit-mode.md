---
description: Bestimmen des Bearbeitungsmodus
title: Festlegen des Bearbeitungsmodus | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- editing data [ADO], edit mode
- ADO, editing data
ms.assetid: 4c7e010d-08cd-4e22-9b32-23c36f02f88c
author: rothja
ms.author: jroth
ms.openlocfilehash: 1b0a6d6642e17841b8a974efa8d497cdc12203fe
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100033250"
---
# <a name="determining-edit-mode"></a>Bestimmen des Bearbeitungsmodus
ADO verwaltet einen Bearbeitungs Puffer, der dem aktuellen Datensatz zugeordnet ist. Die **EditMode** -Eigenschaft gibt an, ob an diesem Puffer Änderungen vorgenommen wurden oder ob ein neuer Datensatz erstellt wurde. Verwenden Sie **EditMode** , um den Bearbeitungsstatus des aktuellen Datensatzes zu bestimmen. Sie können auf ausstehende Änderungen testen, wenn ein Bearbeitungsvorgang unterbrochen wurde, und feststellen, ob Sie die **Update** -oder **CancelUpdate** -Methode verwenden müssen.  
  
 **EditMode** gibt eine der **EditModeEnum** -Konstanten zurück, die in der folgenden Tabelle aufgeführt sind.  
  
|Konstante|BESCHREIBUNG|  
|--------------|-----------------|  
|**adEditNone**|Gibt an, dass kein Bearbeitungsvorgang ausgeführt wird.|  
|**adEditInProgress**|Gibt an, dass die Daten im aktuellen Datensatz geändert, aber nicht gespeichert wurden.|  
|**adEditAdd**|Gibt an, dass die **AddNew** -Methode aufgerufen wurde und der aktuelle Datensatz im Kopier Puffer ein neuer Datensatz ist, der nicht in der Datenbank gespeichert wurde.|  
|**adeditdelete**|Gibt an, dass der aktuelle Datensatz gelöscht wurde.|  
  
 **EditMode** kann nur dann einen gültigen Wert zurückgeben, wenn ein aktueller Datensatz vorhanden ist. **EditMode** gibt einen Fehler zurück, wenn **BOF** oder **EOF** **true** ist oder wenn der aktuelle Datensatz gelöscht wurde.
