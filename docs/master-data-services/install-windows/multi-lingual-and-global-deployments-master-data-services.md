---
title: Mehrsprachige und globale bereit Stellungen
description: Master Data Services unterstützt die Bereitstellung von Komponenten und Tools in allen von SQL Server unterstützten Sprachen.
ms.custom: seo-lt-2019
ms.date: 12/13/2019
ms.prod: sql
ms.reviewer: ''
ms.technology: master-data-services
ms.topic: conceptual
ms.assetid: c3d485f8-867c-4aa2-a90d-f38fda192534
author: lrtoyou1223
ms.author: lle
ms.openlocfilehash: 02cd12f7216e3f73c31be931ab23d47450bcdaaa
ms.sourcegitcommit: f7ac1976d4bfa224332edd9ef2f4377a4d55a2c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85883846"
---
# <a name="multi-lingual-and-global-deployments-master-data-services"></a>Mehrsprachige und globale Bereitstellungen (Master Data Services)

[!INCLUDE [SQL Server Windows Only - ASDBMI ](../../includes/applies-to-version/sql-windows-only-asdbmi.md)]

  [!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)] unterstützt die Bereitstellung von Komponenten und Tools in allen von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]unterstützten Sprachen. Weitere Informationen finden Sie unter [Local Language Versions in SQL Server](../../sql-server/install/local-language-versions-in-sql-server.md).  
  
## <a name="how-languages-are-used"></a>Vorgehensweise bei der Verwendung von Sprachen  
 In der folgenden Tabelle wird die Sprachunterstützung für die Komponenten und Tools von [!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)] beschrieben.  
  
|Komponente oder Tool|Beschreibung|  
|-----------------------|-----------------|  
|[!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)] -Setup|Wählen Sie das englische Setupprogramm aus, wenn die [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] -Webanwendung in anderen Sprachen als der Setupsprache verfügbar sein und unterstützt werden soll. Weitere Informationen finden Sie in der Beschreibung zu [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] unten.|  
|[!INCLUDE[ssMDScfgmgr](../../includes/ssmdscfgmgr-md.md)]|Die Setupsprache bestimmt die Sprache von [!INCLUDE[ssMDScfgmgr](../../includes/ssmdscfgmgr-md.md)] . Wenn Sie Deutsch als Setupsprache auswählen, ist [!INCLUDE[ssMDScfgmgr](../../includes/ssmdscfgmgr-md.md)] auf dem betreffenden Computer z. B. in Deutsch verfügbar.|  
|[!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)]|Wenn Sie das Setup auf Englisch ausführen, wird die [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] -Webanwendung in allen Anwendungssprachen bereitgestellt und unterstützt. [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] kann in jeder dieser Anwendungssprachen angezeigt werden und akzeptiert gebietsschemaspezifische Eingaben auf Grundlage der Spracheinstellungen des Clientwebbrowsers. Wenn die Spracheinstellungen für eine nicht unterstützte Anwendungssprache konfiguriert werden, verwendet [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] standardmäßig Englisch.<br /><br /> Wenn Sie das Setup in einer anderen Sprache als Englisch ausführen, sind Ressourcen für alle anderen Anwendungssprachen enthalten. Bei diesem Szenario kann [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] von den Clients jedoch nicht in einer anderen Sprache als der ausgewählten Setupsprache verwendet werden. Wenn Sie versuchen, in einer anderen Sprache als der Setupsprache auf [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] zuzugreifen, könnten Probleme bei der Anzeige und Eingabe von Daten in die Anwendung auftreten.|  
|[!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)]-Datenbank|Die Informationen in der [!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)] -Datenbank sind nicht spezifisch für ein bestimmtes Gebietsschema. Dadurch kann [!INCLUDE[ssMDSmdm](../../includes/ssmdsmdm-md.md)] selbst bestimmen, wie Informationen, z. B. Datumsangaben und Zahlen, in dem durch die Spracheinstellungen im Clientwebbrowser festgelegten Format angezeigt werden.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Installieren von Master Data Services](../../master-data-services/install-windows/install-master-data-services.md)  
  
  
