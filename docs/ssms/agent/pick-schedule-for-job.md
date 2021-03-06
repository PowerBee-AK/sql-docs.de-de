---
description: Zeitplan für Auftrag auswählen
title: Zeitplan für Auftrag auswählen
ms.custom: seo-lt-2019
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: sql-tools
ms.technology: ssms
ms.topic: conceptual
f1_keywords:
- sql13.ag.job.pickscheduleforjob.f1
helpviewer_keywords:
- Pick Schedule for Job dialog box
ms.assetid: 6de2025d-c25c-47b9-9a25-18c294935c15
author: markingmyname
ms.author: maghan
ms.reviewer: ''
monikerRange: = azuresqldb-mi-current || >= sql-server-2016
ms.openlocfilehash: 860d949cf17c41daee42a3261785e5b067b32ce0
ms.sourcegitcommit: 1a544cf4dd2720b124c3697d1e62ae7741db757c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "97474421"
---
# <a name="pick-schedule-for-job"></a>Zeitplan für Auftrag auswählen
[!INCLUDE [SQL Server SQL MI](../../includes/applies-to-version/sql-asdbmi.md)]

> [!IMPORTANT]  
> In [Azure SQL Managed Instance](/azure/sql-database/sql-database-managed-instance) werden derzeit die meisten, aber nicht alle, SQL Server-Agent-Features unterstützt. Details dazu finden Sie unter [Unterschiede zwischen Azure SQL Managed Instance und SQL Server](/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent).

Wählen Sie in diesem Dialogfeld einen vorhandenen Zeitplan für den [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Agent-Auftrag aus.  
  
## <a name="options"></a>Optionen  
**Verfügbare Zeitpläne**  
Führt die verfügbaren Zeitpläne für diesen Auftrag auf. Weil ein Auftrag und ein Zeitplan denselben Besitzer haben müssen, enthält diese Liste nur Zeitpläne, die dem Besitzer des Auftrags gehören.  
  
**Name**  
Zeigt den Namen des Zeitplans an.  
  
**Enabled**  
Ausgewählt, wenn der Zeitplan aktiviert ist.  
  
**Beschreibung**  
Beschreibt die Bedingungen, unter denen der Zeitplan den Auftrag ausführt.  
  
**Aufträge im Zeitplan**  
Listet die Auftragsnummern auf, die an den Zeitplan angefügt sind. Wenn Sie auf eine Nummer klicken, zeigen Sie die Eigenschaften des Auftrags an.  
  
**Eigenschaften**  
Öffnet das Dialogfeld **Eigenschaften des Auftragszeitplans** , in dem Sie Informationen zum Zeitplan anzeigen können.  
  
## <a name="see-also"></a>Weitere Informationen  
[Anlegen und Zuweisen von Zeitplänen zu Aufträgen](../../ssms/agent/create-and-attach-schedules-to-jobs.md)  
