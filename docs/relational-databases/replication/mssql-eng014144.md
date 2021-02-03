---
description: MSSQL_ENG014144
title: MSSQL_ENG014144 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
helpviewer_keywords:
- MSSQL_ENG014144 error
ms.assetid: fdc744d5-530e-48c4-9420-cca032fd482b
author: MashaMSFT
ms.author: mathoma
monikerRange: =azuresqldb-mi-current||>=sql-server-2016
ms.openlocfilehash: 892f71b9fbfafd6226b32e2f23d8bb85a4d9fe38
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99198793"
---
# <a name="mssql_eng014144"></a>MSSQL_ENG014144
[!INCLUDE [SQL Server SQL MI](../../includes/applies-to-version/sql-asdbmi.md)]
    
## <a name="message-details"></a>Meldungsdetails  
  
|attribute|Wert|  
|-|-|  
|Produktname|SQL Server|  
|Ereignis-ID|14144|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|[!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)]|  
|Symbolischer Name||  
|Meldungstext|Der '%s'-Abonnent kann nicht gelöscht werden. Für ihn sind Abonnements in der %2!s!-Veröffentlichungsdatenbank vorhanden.|  
  
## <a name="explanation"></a>Erklärung  
 Eine [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Instanz, die als Abonnent konfiguriert ist, kann nicht aus der Rolle des Abonnenten entfernt werden, so lange für die Instanz aktive Abonnements konfiguriert sind.  
  
## <a name="user-action"></a>Benutzeraktion  
 Löschen Sie alle zugeordneten Abonnements, bevor Sie versuchen, den Abonnentenstatus der [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Instanz zu ändern:  
  
1.  Führen Sie [sp_helpsubscription &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-helpsubscription-transact-sql.md) in der Publikationsdatenbank auf dem Verleger aus, um nach Abonnements zu suchen.  
  
2.  Führen Sie [sp_dropsubscription &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-dropsubscription-transact-sql.md) in der Publikationsdatenbank aus, um Abonnements zu löschen.  

## <a name="see-also"></a>Weitere Informationen  
 [Fehler- und Ereignisreferenz &#40;Replikation&#41;](../../relational-databases/replication/errors-and-events-reference-replication.md)   
 [Abonnieren von Veröffentlichungen](../../relational-databases/replication/subscribe-to-publications.md)  
  
  
