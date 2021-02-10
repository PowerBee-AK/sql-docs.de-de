---
description: Umgang mit fehlerhaften Updates
title: Umgang mit fehlgeschlagenen Updates | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- updates [ADO], dealing with failed updates
ms.assetid: 299c37bd-19ff-4261-8571-b9665687e075
author: rothja
ms.author: jroth
ms.openlocfilehash: a5ce736c8dd24f2398d7c8c374be260080c32e11
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037640"
---
# <a name="dealing-with-failed-updates"></a>Umgang mit fehlerhaften Updates
Wenn ein Update mit Fehlern beendet wird, hängt die Art und Weise, wie Sie die Fehler beheben, von der Art und dem Schweregrad der Fehler und der Logik der Anwendung ab. Wenn die Datenbank jedoch für andere Benutzer freigegeben wird, besteht ein typischer Fehler darin, dass ein anderer Benutzer das Feld ändert, bevor Sie dies tun. Diese Art von Fehler wird als Konflikt bezeichnet. ADO erkennt diese Situation und meldet einen Fehler.  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn Update Fehler vorliegen, werden Sie in einer Fehler Behandlungs Routine erfasst. Filtern Sie das Recordset mit der adFilterConflictingRecords-Konstante, sodass nur die in Konflikt stehenden Zeilen sichtbar sind. In diesem Beispiel besteht die Fehler Auflösungs Strategie darin, die vor-und Nachnamen des Autors (au_fname und au_lname) zu drucken.  
  
 Der Code zum Benachrichtigen des Benutzers für den Update Konflikt sieht wie folgt aus:  
  
```  
objRs.Filter = adFilterConflictingRecords  
objRs.MoveFirst  
Do While Not objRst.EOF  
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname  
   objRs.MoveNext  
Loop  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [Batchmodus](./batch-mode.md)