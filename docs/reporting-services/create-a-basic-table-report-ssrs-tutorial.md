---
title: Erstellen eines einfachen Tabellenberichts (SSRS-Tutorial) | Microsoft-Dokumentation
description: Verwenden Sie das Berichts-Designer-Tool in Visual Studio bzw. SQL Server Data Tools (SSDT), und erstellen Sie dann einen paginierten SSRS-Bericht (SQL Server Reporting Services).
ms.date: 04/16/2019
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.technology: reporting-services
ms.topic: conceptual
helpviewer_keywords:
- walkthroughs [Reporting Services]
- tutorials [Reporting Services]
- reports [Reporting Services], creating
ms.assetid: 3b539b4b-26f2-4c0b-b506-80f175679a46
author: maggiesMSFT
ms.author: maggies
ms.openlocfilehash: f1549d3ba775d598902fd0fd4b5cc33bab2f54de
ms.sourcegitcommit: 216f377451e53874718ae1645a2611cdb198808a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2020
ms.locfileid: "87245139"
---
# <a name="create-a-basic-table-report-ssrs-tutorial"></a>Erstellen eines einfachen Tabellenberichts (SSRS-Lernprogramm)

In diesem Tutorial verwenden Sie das *Berichts-Designer*-Tool in Visual Studio bzw. SQL Server Data Tools (SSDT). Sie erstellen einen paginierten SQL Server Reporting Services-Bericht (SSRS). Der Bericht enthält eine Abfragetabelle, die aus Daten in der AdventureWorks2016-Datenbank erstellt wurde.

Im Laufe des Tutorials lernen Sie folgende Themen kennen:
  
- Erstellen eines Berichtsprojekts
- Einrichten einer Datenverbindung
- Definieren einer Abfrage
- Hinzufügen eines Tabellendatenbereichs
- Formatieren des Berichts
- Gruppen- und Gesamtsummenfelder
- Vorschauversion des Berichts
- Veröffentlichen des Berichts (optional)

## <a name="requirements"></a>Requirements (Anforderungen)

Ihr System muss die folgenden installierten Komponenten aufweisen, damit dieses Tutorial verwendet werden kann:

- [!INCLUDE[msconame-md](../includes/msconame-md.md)] SQL Server-Datenbank-Engine  
- SQL Server 2016 Reporting Services oder höher (SSRS)
- Die AdventureWorks2016-Datenbank.  Weitere Informationen finden Sie in den [AdventureWorks-Beispieldatenbanken](https://github.com/Microsoft/sql-server-samples/releases).
- [SQL Server Data Tools](../ssdt/download-sql-server-data-tools-ssdt.md) für Visual Studio, zusammen mit der installierten Reporting Services-Erweiterung für den Zugriff auf den *Berichts-Designer*.
  
Sie müssen auch über Leseberechtigung verfügen, um Daten aus der AdventureWorks2016-Datenbank abrufen zu können.

**Ungefähre Dauer dieses Tutorials:** 30 Minuten

## <a name="next-steps"></a>Nächste Schritte

[Lektion 1: Erstellen eines Berichtsserverprojekts &#40;Reporting Services&#41;](lesson-1-creating-a-report-server-project-reporting-services.md)

[Lektion 2: Angeben von Verbindungsinformationen &#40;Reporting Services&#41;](lesson-2-specifying-connection-information-reporting-services.md)

[Lektion 3: Definieren eines Datasets für den Tabellenbericht &#40;Reporting Services&#41;](lesson-3-defining-a-dataset-for-the-table-report-reporting-services.md)

[Lektion 4: Hinzufügen einer Tabelle zum Bericht &#40;Reporting Services&#41;](lesson-4-adding-a-table-to-the-report-reporting-services.md)

[Lesson 5: Formatieren eines Berichts &#40;Reporting Services&#41;](lesson-5-formatting-a-report-reporting-services.md)

[Lektion 6: Hinzufügen von Gruppierungen und Gesamtwerten &#40;Reporting Services&#41;](lesson-6-adding-grouping-and-totals-reporting-services.md)

## <a name="see-also"></a>Weitere Informationen

[Reporting Services-Tutorials](reporting-services-tutorials-ssrs.md) Haben Sie weitere Fragen? [Stellen Sie eine Frage im Reporting Services-Forum](https://go.microsoft.com/fwlink/?LinkId=620231)
