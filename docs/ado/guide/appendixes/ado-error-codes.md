---
description: ADO-Fehler Codes erfassen
title: ADO-Fehler Codes | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 02/15/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- errors [ADO], error codes
ms.assetid: 3aee61c7-a9b7-4596-b78e-5828a00d0281
author: rothja
ms.author: jroth
ms.openlocfilehash: 2d3b0fd0c3a673cc841d7a5318872151bc20b311
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100029504"
---
# <a name="capture-ado-error-codes"></a>ADO-Fehler Codes erfassen
Zusätzlich zu den Anbieter Fehlern, die in den [Fehler](../../reference/ado-api/error-object.md) Objekten der [Fehler](../../reference/ado-api/errors-collection-ado.md) Auflistung zurückgegeben werden, kann ADO selbst Fehler an den Mechanismus zur Ausnahmebehandlung der Laufzeitumgebung zurückgeben. Verwenden Sie den fehlerabfang Mechanismus in ihrer Programmiersprache, wie z. b. die **On Error** -Anweisung in Microsoft® Visual Basic oder den **try-catch-** Block in Microsoft Visual C++®, um ADO-Fehler aufzuzeichnen.

 Eine Liste der ADO-Fehlercodes finden Sie unter [ErrorValueEnum](../../reference/ado-api/errorvalueenum.md).

## <a name="see-also"></a>Weitere Informationen
 [Error Object](../../reference/ado-api/error-object.md) [Errors Collection (ADO)](../../reference/ado-api/errors-collection-ado.md)