---
description: MSSQLSERVER_41030
title: MSSQLSERVER_41030 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 41030 (Database Engine error)
ms.assetid: c85341ae-0fbf-42ae-9275-4cfe678238f0
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 5e091a0e56074657601f23a082ea32bd62128dd9
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99185134"
---
# <a name="mssqlserver_41030"></a>MSSQLSERVER_41030
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]|  
|Ereignis-ID|41030|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|OPEN_CLUSTER_SUB_KEY|  
|Meldungstext|Fehler beim Öffnen des WSFC (Windows Server Failover Clustering)-Registrierungsunterschlüssels '%.*ls' (Fehlercode %d).  Der übergeordnete Schlüssel ist der Clusterstammschlüssel.  Der WSFC-Dienst wird möglicherweise nicht ausgeführt, der Zugriff auf den Dienst ist möglicherweise im aktuellen Zustand nicht möglich, oder die angegebenen Argumente sind ungültig. Wurde die entsprechende Verfügbarkeitsgruppe gelöscht, wird dieser Fehler erwartet. Informationen zu diesem Fehlercode finden Sie in der Dokumentation für die Windows-Entwicklung im Abschnitt zu Systemfehlercodes.|  
  
## <a name="explanation"></a>Erklärung  
Wenn ein WSFC-Cluster zerstört wird, werden alle auf [!INCLUDE[ssHADR](../../includes/sshadr-md.md)] bezogenen Registrierungsschlüssel entfernt.  
  
## <a name="user-action"></a>Benutzeraktion  
Nach dem Neuerstellen eines WSFC-Clusters deaktivieren und aktivieren Sie dann AlwaysOn auf jedem Clusterknoten erneut, auf dem eine [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Instanz für AlwaysOn aktiviert wird. Sie können für diese Aufgabe den [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]-Konfigurations-Manager verwenden.  
  
## <a name="see-also"></a>Weitere Informationen  
[Aktivieren und Deaktivieren von Always On-Verfügbarkeitsgruppen &#40;SQL Server&#41;](~/database-engine/availability-groups/windows/enable-and-disable-always-on-availability-groups-sql-server.md)  
[Windows Server-Failoverclustering &#40;WSFC&#41; mit SQL Server](~/sql-server/failover-clusters/windows/windows-server-failover-clustering-wsfc-with-sql-server.md)  
  
