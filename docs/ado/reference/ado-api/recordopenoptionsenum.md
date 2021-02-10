---
description: RecordOpenOptionsEnum
title: Recordopenoptionsenum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
apitype: COM
f1_keywords:
- RecordOpenOptionsEnum
helpviewer_keywords:
- RecordOpenOptionsEnum enumeration [ADO]
ms.assetid: 9028aba4-90fc-4dfc-88e4-fa8a7b6fedee
author: rothja
ms.author: jroth
ms.openlocfilehash: 087b8bc6540fdfb3e504273ed2e02b71163088fa
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100051821"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum
Gibt Optionen für das Öffnen eines [Datensatzes](./record-object-ado.md)an. Diese Werte können mit oder kombiniert werden.  
  
|Konstante|Wert|BESCHREIBUNG|  
|--------------|-----------|-----------------|  
|**addelta-fetchfields**|0x8000|Gibt dem Anbieter an, dass die dem **Datensatz** zugeordneten Felder anfänglich nicht abgerufen werden müssen, sondern beim ersten Versuch, auf das Feld zuzugreifen, abgerufen werden können. Das Standardverhalten, das durch das Fehlen dieses Flags angegeben wird, besteht darin, alle **Daten Satz** Objekt Felder abzurufen.|  
|**addelta-fetchstream**|0x4000|Gibt dem Anbieter an, dass der dem Datensatz zugeordnete Standard **Daten** Strom anfänglich nicht abgerufen werden muss. Das Standardverhalten, das durch das Fehlen dieses Flags angegeben ist, besteht darin, den dem **Datensatz** -Objekt zugeordneten Standardstream abzurufen.|  
|**adopendasync**|0x1000|Gibt an, dass das **Datensatz** -Objekt im asynchronen Modus geöffnet wird.|  
|**adopteexecutecommand**|0x10000|Gibt an, dass die Quell Zeichenfolge Befehls Text enthält, der ausgeführt werden soll. Dieser Wert entspricht der Option **adCmdText** für **Recordset. Open**.|  
|**adopendrecordunspezifiziert**|-1|Standard. Gibt an, dass keine Optionen angegeben.|  
|**adopendoutput**|0x800000|Gibt an, dass die Quelle auf einen Knoten verweist, der ein ausführbares Skript enthält (z. b.). ASP-Seite), dann enthält der geöffnete **Datensatz** die Ergebnisse des ausgeführten Skripts. Dieser Wert gilt nur für Datensätze, die keine Sammlung sind.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Diese Konstanten haben keine ADO/WFC-Entsprechungen.  
  
## <a name="applies-to"></a>Gilt für  
 [Open-Methode (ADO Record)](./open-method-ado-record.md)