---
title: Installieren von SCOM-Management Packs
description: Führen Sie die folgenden Schritte aus, um die System Center Operations Manager-Management Packs (SCOM) für SQL Server PDW herunterzuladen und zu installieren. Die Management Packs sind erforderlich, um SQL Server PDW von SCOM zu überwachen.
author: mzaman1
ms.prod: sql
ms.technology: data-warehouse
ms.topic: conceptual
ms.date: 04/17/2018
ms.author: murshedz
ms.reviewer: martinle
ms.custom: seo-dt-2019
ms.openlocfilehash: d8f4145b85d505ccdf1d0fe26b22f2cdf02d9e90
ms.sourcegitcommit: 370cab80fba17c15fb0bceed9f80cb099017e000
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "97641493"
---
# <a name="install-sql-server-operations-manager-scom-management-packs-for-analytics-platform-system"></a>Installieren von SQL Server Operations Manager Management Packs (SCOM) für Analytics Platform System
Führen Sie die folgenden Schritte aus, um die System Center Operations Manager-Management Packs (SCOM) für SQL Server PDW herunterzuladen und zu installieren. Die Management Packs sind erforderlich, um SQL Server PDW von SCOM zu überwachen.  
  
## <a name="before-you-begin"></a><a name="BeforeBegin"></a>Vorbereitungen  
**Voraussetzungen**  
  
System Center Operations Manager müssen installiert sein und ausgeführt werden. SQL Server PDW 2012 erfordert System Center Operations Manager 2007 R2, System Center Operations Manager 2012 oder System Center Operations Manager 2012 Service Pack 1.  
  
## <a name="step-1-download-the-management-packs"></a><a name="Step1"></a>Schritt 1: Herunterladen der Management Packs  
Laden Sie für die APS PDW-Arbeitsauslastung das [System Center-Management Pack für den Microsoft Analytics Platform System](https://go.microsoft.com/fwlink/?LinkId=396857)herunter.  
  
Laden Sie für die Geräteverwaltung das [Basis-Management Pack für SQL Server Appliance](/previous-versions/system-center/packs/gg602398(v=technet.10))herunter.  
  
Für ältere Versionen von PDW ohne APS laden Sie das[System Center Monitoring Pack für Microsoft SQL Server 2012 parallel Data Warehouse Appliance](./download-and-apply-microsoft-updates.md?view=aps-pdw-2016-au7&preserve-view=true)herunter.  
  
<!-- MISSING LINKS - For the HDInsight workload, download the [System Center Management Pack for HDInsight](https://go.microsoft.com/fwlink/?LinkId=390208).  -->
  
## <a name="step-2-install-the-management-packs"></a><a name="Step2"></a>Schritt 2: Installieren der Management Packs  
  
### <a name="install-the-sql-server-appliance-base-management-pack"></a>Installieren des Basis-Management Packs für die SQL Server Appliance  
  
1.  Zum Ausführen der Installation Doppelklicken Sie auf das heruntergeladene Basis-Management Pack für SQL Server Appliance.  
  
2.  Akzeptieren Sie den Lizenzvertrag, und klicken Sie auf **weiter**.  
  
    ![Akzeptieren Sie den Lizenzvertrag.](./media/install-the-scom-management-packs/SCOM_licnse_agrmt.png "SCOM_licnse_agrmt")  
  
3.  Wählen Sie Ihren eigenen Installationsordner aus, oder verwenden Sie den Standard-Management Pack-Installationsordner.  
  
    ![Installationsordner auswählen](./media/install-the-scom-management-packs/SCOM_licnse_agrmt2.png "SCOM_licnse_agrmt2")  
  
4.  Klicken Sie auf **Installieren**.  
  
    ![Screenshot des Assistenten zum Überprüfen der Basis Überwachung von SQL Server Appliance im MP-Installationsschritt, bei dem die Option "Install" rot markiert ist.](./media/install-the-scom-management-packs/SCOM_licnse_agrmt3.png "SCOM_licnse_agrmt3")  
  
5.  Klicken Sie auf **Schließen**.  
  
    ![Klicken Sie auf Schließen](./media/install-the-scom-management-packs/SCOM_licnse_agrmt4.png "SCOM_licnse_agrmt4")  
  
### <a name="install-the-monitoring-pack-for-sql-server-pdw-appliance"></a>Installieren des Überwachungs Pakets für SQL Server PDW Appliance  
  
1.  Zum Ausführen der Installation Doppelklicken Sie auf das heruntergeladene SQL Server PDW Appliance-Management Pack.  
  
2.  Akzeptieren Sie den Lizenzvertrag, und klicken Sie auf **weiter**.  
  
    ![Akzeptieren der Lizenzbedingungen](./media/install-the-scom-management-packs/SCOM_licnse_agmtB.png "SCOM_licnse_agmtB")  
  
3.  Wählen Sie das Verzeichnis aus, in dem die extrahierten Dateien gespeichert werden. Standardmäßig wird der Standard-Management Pack-Installationsordner angezeigt. Wählen Sie den Standardwert aus, oder wählen Sie einen eigenen Installationsordner aus.  
  
    ![Installationsordner auswählen](./media/install-the-scom-management-packs/SCOM_licnse_agmtB1.png "SCOM_licnse_agmtB1")  
  
4.  Klicken Sie auf **Installieren**.  
  
    ![Screenshot des Assistenten für den pdwmp-Installer im Installationsschritt bestätigen, dass die Option installieren in rot angezeigt wird.](./media/install-the-scom-management-packs/SCOM_licnse_agmtB2.png "SCOM_licnse_agmtB2")  
  
5.  Klicken Sie auf **Schließen**.  
  
    ![Installation abgeschlossen](./media/install-the-scom-management-packs/SCOM_licnse_agmtB3.png "SCOM_licnse_agmtB3")  
  
## <a name="next-step"></a>Nächster Schritt  
Nachdem Sie die Management Packs installiert haben, fahren Sie mit dem nächsten Schritt fort: [Importieren des SCOM-Management Packs für PDW &#40;Analytics Platform System&#41;](import-the-scom-management-pack-for-pdw.md).  
  
<!-- MISSING LINKS ## See Also  
[Common Metadata Query Examples &#40;SQL Server PDW&#41;](../sqlpdw/common-metadata-query-examples-sql-server-pdw.md)  -->