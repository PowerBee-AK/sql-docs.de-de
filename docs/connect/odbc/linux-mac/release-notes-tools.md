---
title: Versionshinweise zu „mssql-tools“ in Linux und macOS
description: Hier finden Sie Informationen zu Neuerungen und Änderungen in veröffentlichten Versionen der Microsoft SQL Server-Tools.
ms.custom: ''
ms.date: 01/29/2021
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: v-daenge
ms.technology: connectivity
ms.topic: conceptual
author: v-zhangw
ms.author: v-zhangw
manager: kenvh
ms.openlocfilehash: 75f1144e84792b3c9361dcab74dcdbcb7b072268
ms.sourcegitcommit: f30b5f61c514437ea58acc5769359c33255b85b5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "99075922"
---
# <a name="release-notes-for-the-microsoft-sql-server-tools-on-linux-and-macos"></a>Versionshinweise zu Microsoft SQL Server-Tools in Linux und macOS

[!INCLUDE[Driver_ODBC_Download](../../../includes/driver_odbc_download.md)]

In diesem Artikel werden die Neuerungen der versionierten Releases der [!INCLUDE[msCoName](../../../includes/msconame_md.md)] SQL Server-Tools in Linux und macOS aufgelistet und beschrieben.

## <a name="17711-january-2021"></a>17.7.1.1, Januar 2021

| Neues Feature | Details |
| :------------ | :------ |
| Sqlcmd Bugfix | Ein Fehler bei der Umleitung von Eingaben und leere Zeilen, die zu einer wiederholten Ausführung geführt haben, wurden behoben. |
| Sqlcmd Bugfix | Eine fehlerhafte Fehlerberichterstattung für r-, p-, X- und k-Optionen bei bestimmten Formatierungen wurde behoben. |
| Sqlcmd -z/-Z „Password“ Option | Dieses Feature wird ab sofort unterstützt. |
| &nbsp; | &nbsp; |

## <a name="17611-july-2020"></a>17.6.1.1 – Juli 2020

| Neues Feature | Details |
| :------------ | :------ |
| Sqlcmd-Befehlszeilenparser aktualisiert | Es wurden Fehler aufgrund eines unerwarteten Verhaltens behoben, das bei der Verwendung bestimmter Optionen in unterschiedlicher Reihenfolge aufgetreten ist. |
| Sqlcmd-Fehlermeldungen aktualisiert | Es wurden verschiedene Inkonsistenzen bei der Rückgabe von Fehlern in sqlcmd korrigiert. |
| Option „-Y“ von sqlcmd korrigiert | Es wurde ein Problem behoben, bei dem die Option „-Y“ wirkungslos war. |
| Abgeschnittene Sqlcmd-Spaltennamen korrigiert | Es wurde ein Problem behoben, bei dem Spaltennamen falsch abgeschnitten wurden. |
| Linux-Exitcodes von sqlcmd | Es wurde ein Problem behoben, bei dem der Prozessexitcode in Linux fehlte. |
| &nbsp; | &nbsp; |

## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über das Herstellen einer Verbindung mit [BCP](connecting-with-bcp.md) und [SQLCMD](connecting-with-sqlcmd.md).
