---
description: MSSQLSERVER_1406
title: MSSQLSERVER_1406 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 1406 (Database Engine error)
ms.assetid: 915f97de-9b74-41f8-8bd5-b2d061416718
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: c5d7fe3f66ea581305f985e25cc1a2c30c1809e4
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99197017"
---
# <a name="mssqlserver_1406"></a>MSSQLSERVER_1406
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|1406|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|DBM_BADSTATEFORFORCESERVICE|  
|Meldungstext|Der Dienst kann nicht auf sichere Weise erzwungen werden. Entfernen Sie die Datenbankspiegelung, und stellen Sie die "%.*ls"-Datenbank wieder her, um Zugriff zu erhalten.|  
  
## <a name="explanation"></a>Erklärung  
Der Dienst kann von [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] nicht erzwungen werden, da mit dem Spiegelungsstatus nicht garantiert werden kann, dass der erzwungene Dienstvorgang ordnungsgemäß funktioniert.  
  
## <a name="user-action"></a>Benutzeraktion  
Entfernen Sie die Datenbankspiegelung. Sie können anschließend die Spiegeldatenbank wiederherstellen, um Zugriff zu erhalten.  
  
## <a name="see-also"></a>Weitere Informationen  
[Erzwingen des Diensts in einer Datenbank-Spiegelungssitzung &#40;Transact-SQL&#41;](~/database-engine/database-mirroring/force-service-in-a-database-mirroring-session-transact-sql.md)  
[Entfernen der Datenbankspiegelung &#40;SQL Server&#41;](~/database-engine/database-mirroring/removing-database-mirroring-sql-server.md)  
  
