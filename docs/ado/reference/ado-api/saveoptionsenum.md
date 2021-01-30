---
description: SaveOptionsEnum
title: Saveoptionsenum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- SaveOptionsEnum
helpviewer_keywords:
- SaveOptionsEnum enumeration [ADO]
ms.assetid: 59339100-6e29-48d1-aea3-6873796d186b
author: rothja
ms.author: jroth
ms.openlocfilehash: e80e94e4ccc98faa7cf825facc62df01395855a2
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99170320"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum
Gibt an, ob eine Datei beim Speichern aus einem [Streamobjekt](./stream-object-ado.md) erstellt oder überschrieben werden soll. Die Werte können " **adsavecreatenotexist** " oder " **adsavecreateüberschreibung**" lauten.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**adsavecreatenotexist**|1|Standard. Erstellt eine neue Datei, wenn die durch den *filename* -Parameter angegebene Datei nicht bereits vorhanden ist.|  
|**adsavecreateüberschreibung**|2|Überschreibt die Datei mit den Daten aus dem momentan geöffneten Daten **Strom** Objekt, wenn die durch den *filename* -Parameter angegebene Datei bereits vorhanden ist. Wenn die durch den *filename* -Parameter angegebene Datei nicht vorhanden ist, wird eine neue Datei erstellt.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Diese Konstanten haben keine ADO/WFC-Entsprechungen.  
  
## <a name="applies-to"></a>Gilt für  
 [SaveToFile-Methode](./savetofile-method.md)