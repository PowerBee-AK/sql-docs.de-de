---
description: MSSQL_ENG020572
title: MSSQL_ENG020572 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: reference
helpviewer_keywords:
- MSSQL_ENG020572 error
ms.assetid: 636566db-ffcf-4109-8c11-15b8c7cb9cd9
author: MashaMSFT
ms.author: mathoma
monikerRange: =azuresqldb-mi-current||>=sql-server-2016
ms.openlocfilehash: 72b71abce767a2e988f8608757e34d76dd5fff96
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205584"
---
# <a name="mssql_eng020572"></a>MSSQL_ENG020572
[!INCLUDE [SQL Server SQL MI](../../includes/applies-to-version/sql-asdbmi.md)]
    
## <a name="message-details"></a>Meldungsdetails  
  
|attribute|Wert|  
|-|-|  
|Produktname|SQL Server|  
|Ereignis-ID|20572|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|[!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)]|  
|Symbolischer Name||  
|Meldungstext|Das Abonnement des Abonnenten '%s' für den '%s'-Artikel in der '%s'-Veröffentlichung wurde nach einem Datenüberprüfungsfehler neu initialisiert.|  
  
## <a name="explanation"></a>Erklärung  
 Die Daten des Abonnenten wurden gegen die Daten des Verlegers abgeglichen, und es wurde keine Übereinstimmung der Daten festgestellt. Daher konnte die Überprüfung nicht erfolgreich abgeschlossen werden. Bei der Angabe zur Ausführung einer Überprüfung haben Sie die Option aktiviert, dass im Falle eines Fehlers bei der Überprüfung eine erneute Initialisierung des Abonnements erfolgen soll. Für eine erneute Initialisierung des Abonnements muss eine neue Momentaufnahme auf dem Abonnenten angewendet werden. Weitere Informationen zur Überprüfung finden Sie unter [Validate Replicated Data](../../relational-databases/replication/validate-data-at-the-subscriber.md).  
  
## <a name="user-action"></a>Benutzeraktion  
 Die Daten auf dem Verleger und auf dem Abonnenten stimmen überein, nachdem die neue Momentaufnahme auf dem Abonnenten angewendet wurde.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Fehler- und Ereignisreferenz &#40;Replikation&#41;](../../relational-databases/replication/errors-and-events-reference-replication.md)  
  
  
