---
description: MSSQLSERVER_17194
title: MSSQLSERVER_17194 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
f1_keywords:
- "17194"
helpviewer_keywords:
- 17194 (Database Engine error)
ms.assetid: 0d03eb20-28a7-4ceb-8903-7f9420a620f7
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: aea38f7ca72e611ebfe7c0f5eb530ac9f25ce962
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99196724"
---
# <a name="mssqlserver_17194"></a>MSSQLSERVER_17194
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|17194|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name||  
|Meldungstext|Der Server konnte die für das Anmelden erforderliche SSL-Anbieterbibliothek nicht laden. Die Verbindung wurde geschlossen. SSL wird zum Verschlüsseln der Anmeldesequenz oder der gesamten Kommunikation verwendet, je nach der vom Administrator festgelegten Serverkonfiguration. Weitere Informationen zu dieser Fehlermeldung finden Sie in der Onlinedokumentation:  0xXXXX. [CLIENT: 11.11.11.11]|  
  
## <a name="explanation"></a>Erklärung  
Mit diesem Fehler wird angegeben, dass die Verbindung vom Client geschlossen wurde. Dieser Fehler ist möglicherweise darauf zurückzuführen, dass das Verbindungstimeout abgelaufen ist. In der Fehlermeldung wird ein Wert des Betriebssystems angezeigt, mit dem das zugrunde liegende Problem beschrieben wird.  
  
## <a name="user-action"></a>Benutzeraktion  
Wenn der Fehlercode in der Meldung 0x2746 lautet (Dezimalwert 10054), bedeutet dies, dass die Verbindung durch den Client zurückgesetzt wurde. Dies ist normalerweise auf ein Timeout zurückzuführen. Wenn Sie den Fehler beheben möchten, erhöhen Sie das Verbindungstimeout für den Client bzw. das aufrufende Programm.  
  
Verwenden Sie zum Bestimmen einer möglichen Lösung für weitere Fehlermeldungswerte den Betriebssystembefehl **net helpmsg**, und geben Sie den Dezimalwert des Fehlercodes an.  
  
Weitere Informationen zum Herstellen einer Verbindung mit einer Instanz von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] finden Sie unter [Server-Netzwerkkonfiguration](~/database-engine/configure-windows/server-network-configuration.md) und [Client-Netzwerkkonfiguration](~/database-engine/configure-windows/client-network-configuration.md).  
  
## <a name="internal-only"></a>Nur intern  
