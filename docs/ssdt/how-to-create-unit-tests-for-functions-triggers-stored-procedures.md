---
title: Erstellen von SQL Server-Komponententests für Funktionen, Trigger und gespeicherte Prozeduren
description: Hier erfahren Sie, wie Sie SQL Server-Objekt-Explorer verwenden, um einen SQL Server-Komponententest aus einer Datenbankfunktion, einem Trigger oder einer gespeicherten Prozedur zu erstellen.
ms.prod: sql
ms.technology: ssdt
ms.topic: conceptual
ms.assetid: bda57c10-a1ab-4a1a-8a71-42085a3cb793
author: markingmyname
ms.author: maghan
ms.reviewer: “”
ms.custom: seo-lt-2019
ms.date: 02/09/2017
ms.openlocfilehash: 2f99946dfb56e3fc1e3e67f42ca93ff5daa11cab
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100018270"
---
# <a name="how-to-create-sql-server-unit-tests-for-functions-triggers-and-stored-procedures"></a>Gewusst wie: Erstellen von SQL Server-Komponententests für Funktionen, Trigger und gespeicherte Prozeduren

Sie können Komponententests schreiben, durch die Änderungen an beliebigen Datenbankobjekten ausgewertet werden. SQL Server Data Tools bietet jedoch zusätzliche Unterstützung für das Erstellen von Tests für Datenbankfunktionen, Triggern und gespeicherten Prozeduren von einem Datenbankprojektnoten im SQL Server-Objekt-Explorer aus. Transact\-SQL-Codestubs können automatisch generiert werden, damit Sie diese anpassen können.  
  
### <a name="to-create-a-sql-server-unit-test-from-a-function-trigger-or-stored-procedure"></a>So erstellen Sie einen SQL Server-Komponententest von Funktionen, Triggern oder gespeicherten Prozeduren  
  
1.  Ein Beispiel zum Hinzufügen eines Komponententests zu einer gespeicherten Prozedur finden Sie unter [Exemplarische Vorgehensweise: Erstellen und Ausführen eines Server-Komponententests](../ssdt/walkthrough-creating-and-running-a-sql-server-unit-test.md) im Abschnitt „So erstellen Sie einen SQL Server-Komponententest für die gespeicherten Prozeduren“.  
  
    Die Testbedingung Nicht eindeutig ist die Standardbedingung, die jedem Test hinzugefügt wird. Diese Testbedingung wird eingeschlossen, um anzuzeigen, dass die Testüberprüfung nicht implementiert wurde. Löschen Sie diese Testbedingung aus dem Test, nachdem Sie weitere Testbedingungen hinzugefügt haben. Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Testbedingungen zu SQL Server-Komponententests](../ssdt/how-to-add-test-conditions-to-sql-server-unit-tests.md).  
  
## <a name="see-also"></a>Weitere Informationen  
[Erstellen und Definieren von SQL Server-Komponententests](../ssdt/creating-and-defining-sql-server-unit-tests.md)  
[Vorgehensweise: Erstellen eines leeren SQL Server-Komponententests](../ssdt/how-to-create-an-empty-sql-server-unit-test.md)  
  
