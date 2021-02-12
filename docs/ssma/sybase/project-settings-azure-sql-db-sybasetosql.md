---
description: Projekteinstellungen (Azure SQL-Datenbank) (sybasedesql)
title: Projekteinstellungen (Azure SQL-Datenbank) (sybasedesql) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: ssma
ms.topic: conceptual
ms.assetid: 57002374-0d4d-43c1-b4e9-cbec02355a9c
author: nahk-ivanov
ms.author: alexiva
ms.openlocfilehash: b532fddbc5eda07ab38aedcb806347846cc0ac59
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100068765"
---
# <a name="project-settings-azure-sql-database--sybasetosql"></a>Projekteinstellungen (Azure SQL-Datenbank) (sybasedesql)
Mit den Azure SQL-Datenbankprojekt Einstellungen können Sie das Azure SQL-Daten Bank Suffix konfigurieren, das im Verbindungs Dialogfeld hinzugefügt werden soll, und die Implementierung des Takt Mechanismus in der Azure SQL-Datenbankverbindung  
  
Der Bereich Azure SQL-Datenbank ist in den Dialogfeldern **Projekteinstellungen** und **Standard Projekteinstellungen** verfügbar.  
  
-   Verwenden Sie das Dialogfeld Projekteinstellungen, um Konfigurationsoptionen für das aktuelle Projekt festzulegen. Um **auf die Azure** SQL-Datenbankeinstellungen zuzugreifen, wählen Sie im Menü Extras die Option **Projekteinstellungen** aus, klicken Sie unten im linken Bereich auf **Allgemein** , und wählen Sie dann **Azure SQL-Datenbank** aus.  
  
-   Verwenden Sie das Dialogfeld Standard Projekteinstellungen, um Konfigurationsoptionen für alle Projekte festzulegen. Um auf die Azure SQL-Datenbankeinstellungen zuzugreifen, wählen Sie **im Menü Extras** die Option **defaultproject Settings** aus, klicken Sie unten im linken Bereich auf **Allgemein** , und wählen Sie dann **Azure SQL-Datenbank** aus.  
  
## <a name="connectivity"></a>Konnektivität  
**Taktintervall**  
  
Gibt ein Zeitintervall an, das für den Takt Mechanismus verwendet wird, um die Azure SQL-Datenbankverbindung im Format "Minuten: Sekunden" zu wahren.  
  
**Standardwert**: "4:45"  
  
Der Wert muss im Format "m:SS" angegeben werden (z. b. "4:45" oder "0:50").  
  
**Azure SQL-Datenbank-Server Suffix**  
  
Gibt ein Azure SQL-Datenbankserver-Suffix an.  
  
**Standardwert**: "Database.Windows.net".  
  
