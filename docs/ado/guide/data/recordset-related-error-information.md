---
description: Fehlerinformationen in Bezug auf Recordsets
title: Recordset-Related Fehlerinformationen | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- Recordset-related errors [ADO]
- errors [ADO], Recordset-related
ms.assetid: 7e103574-59ad-4790-b5f9-fa8d715e711e
author: rothja
ms.author: jroth
ms.openlocfilehash: 2fcd596455cc1074d46ea6ee45d6c1f037553741
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100037100"
---
# <a name="recordset-related-error-information"></a>Fehlerinformationen in Bezug auf Recordsets
Während der Batch Verarbeitung stellt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen über die einzelnen Datensätze im **Recordset** bereit. Bevor ein Batch Update durchgeführt wird, gibt die **Status** -Eigenschaft des **Recordsets** Informationen zu Datensätzen wieder, die hinzugefügt, geändert und gelöscht werden sollen. Nachdem **UpdateBatch** aufgerufen wurde, gibt die Eigenschaft **Status** an, dass der Vorgang erfolgreich war oder fehlgeschlagen ist. Wenn Sie von Datensatz zu Datensatz im **Recordset** wechseln, ändert sich der Wert der **Status** -Eigenschaft, um den Status des aktuellen Datensatzes zu beschreiben.
