---
title: Aktivieren oder Deaktivieren des Sammelns von Nutzungsdaten und des Erstellens von Absturzberichten
description: In diesem Artikel ist erläutert, wie Sie steuern, ob Nutzungs- und Absturzdaten gesammelt und an Microsoft gesendet werden.
ms.prod: azure-data-studio
ms.technology: azure-data-studio
ms.topic: how-to
author: markingmyname
ms.author: maghan
ms.reviewer: alayu, maghan, sstein
ms.custom: seodec18; seo-lt-2019
ms.date: 09/24/2018
ms.openlocfilehash: 5ef44a7e2981d98c749e25692e667ae71b42843d
ms.sourcegitcommit: 63aef5a96905f0b026322abc9ccb862ee497eebe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "91363887"
---
# <a name="enable-or-disable-usage-data-collection-for-azure-data-studio"></a>Aktivieren oder Deaktivieren der Sammlung von Nutzungsdaten für Azure Data Studio

## <a name="how-to-disable-telemetry-reporting"></a>So deaktivieren Sie die Erstellung von Telemetrieberichten

Azure Data Studio sammelt Nutzungsdaten und sendet diese an zur Verbesserung der Produkte und Dienste an Microsoft. Um mehr zu erfahren, lesen Sie die [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkID=528096&clcid=0x409).

Wenn Sie keine Nutzungsdaten an Microsoft senden möchten, legen Sie die Einstellung *telemetry.enableTelemetry* auf *false* fest.

Fügen Sie unter **Datei** > **Einstellungen** > **Einstellungen** die folgende Option hinzu, um alle Telemetrieereignisse von Azure Data Studio zu unterdrücken:

```json
    "telemetry.enableTelemetry": false
```

**Wichtiger Hinweis**: Damit diese Option wirksam wird, ist ein Neustart von Azure Data Studio erforderlich. 

## <a name="how-to-disable-crash-reporting"></a>So deaktivieren Sie die Erstellung von Absturzberichten

Um die Erstellung von Absturzberichten zu deaktivieren, fügen Sie über **Datei** > **Einstellungen** > **Einstellungen** die folgende Option hinzu:

```json
    "telemetry.enableCrashReporter": false
```

**Wichtiger Hinweis**: Damit diese Option wirksam wird, ist ein Neustart von Azure Data Studio erforderlich.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Arbeitsbereich- und Benutzereinstellungen](settings.md)
