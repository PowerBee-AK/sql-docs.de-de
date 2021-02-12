---
title: Überwachen eines Clusters mit einem Grafana-Dashboard
titleSuffix: SQL Server Big Data Clusters
description: Überwachen eines Clusters mit einem Grafana-Dashboard in einem SQL Server 2019-Big Data-Cluster.
author: cloudmelon
ms.author: melqin
ms.reviewer: mikeray
ms.metadata: seo-lt-2019
ms.date: 09/22/2020
ms.topic: conceptual
ms.prod: sql
ms.technology: big-data-cluster
ms.openlocfilehash: 6b9e97e90e844391f62d920b64f7a09de5b6e7ea
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100047730"
---
# <a name="monitor-cluster-with-azdata-and-grafana-dashboard"></a>Überwachen eines Clusters mit azdata und einem Grafana-Dashboard

In diesem Artikel wird beschrieben, wie Sie eine Anwendung in einem Big Data-Cluster in SQL Server überwachen.

## <a name="prerequisites"></a>Voraussetzungen

- [SQL Server 2019: Big Data-Cluster](deployment-guidance.md)
- [Befehlszeilen-Hilfsprogramm „azdata“](../azdata/install/deploy-install-azdata.md)

## <a name="capabilities"></a>Funktionen

In SQL Server 2019 können Sie Ihre Anwendung erstellen, löschen, beschreiben, initialisieren, auflisten und aktualisieren. In der folgenden Tabelle werden die Befehle für die Anwendungsbereitstellung beschrieben, die Sie mit **azdata** verwenden können.

|Get-Help |BESCHREIBUNG |
|:---|:---|
|`azdata bdc endpoint list` | Listet die Endpunkte für den Big Data-Cluster auf. |


Sie können das folgende Beispiel verwenden, um den Endpunkt des **Grafana-Dashboards** aufzulisten:

```bash
azdata bdc endpoint list --endpoint-name metricsui 
```

In der Ausgabe wird der Endpunkt angegeben, den Sie für die Anmeldung mit dem Benutzernamen und dem Kennwort Ihres Clusters verwenden können. 

![Grafana-Dashboard](media/big-data-cluster-monitor-apps/grafana-dashboard-endpoint.png)

Die Werte für `nodeMetricsUrl` und `sqlMetricsUrl` verweisen auf ein Grafana-Dashboard zur Überwachung von Kubernetes-Knotenmetriken und Big Data-Cluster-Dienstmetriken:

![Grafana-Dashboard](./media/view-cluster-status/grafana-dashboard.png)

![SQL](./media/view-cluster-status/grafana-sql-status.png)



## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu [!INCLUDE[big-data-clusters-2019](../includes/ssbigdataclusters-ss-nover.md)] finden Sie unter [Was sind [!INCLUDE[big-data-clusters-2019](../includes/ssbigdataclusters-ver15.md)]?](big-data-cluster-overview.md).