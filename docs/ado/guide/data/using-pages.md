---
description: Verwenden von Seiten
title: Verwenden von Seiten | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- PageSize property [ADO]
- pages [ADO]
- Recordset object [ADO]
- AbsolutePage property [ADO]
- PageCount property [ADO]
ms.assetid: 442b08c5-ccc7-4192-a1cc-22f250867782
author: rothja
ms.author: jroth
ms.openlocfilehash: aae6cbd7d843771fbf88d6d257706ce66e424745
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100036760"
---
# <a name="using-pages"></a>Verwenden von Seiten
Verwenden Sie die **PageCount** -Eigenschaft, um zu bestimmen, wie viele Datenseiten im **Recordset** -Objekt vorliegen. *Seiten* sind Gruppen von Datensätzen, deren Größe der **PageSize** -Eigenschaften Einstellung gleicht. Auch wenn die letzte Seite unvollständig ist, weil weniger Datensätze als der **PageSize** -Wert vorhanden sind, zählt sie als zusätzliche Seite im Wert der **PageCount** . Wenn das **Recordset** -Objekt diese Eigenschaft nicht unterstützt, ist **Page count** -1, um anzugeben, dass die **PageCount** -Eigenschaft unbestimmbar ist.  
  
 Verwenden Sie die **PageSize** -Eigenschaft, um zu bestimmen, wie viele Datensätze eine logische Datenseite bilden. Durch das Festlegen einer Seitengröße können Sie die **AbsolutePage** -Eigenschaft verwenden, um zum ersten Datensatz einer bestimmten Seite zu wechseln. Dies ist in Webserver Szenarios nützlich, wenn Sie es dem Benutzer ermöglichen möchten, Daten zu durchlaufen und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.  
  
 Diese Eigenschaft kann jederzeit festgelegt werden, und ihr Wert wird zum Berechnen der Position des ersten Datensatzes einer bestimmten Seite verwendet.  
  
 Verwenden Sie die **AbsolutePage** -Eigenschaft, um die Seitenzahl zu identifizieren, auf der sich der aktuelle Datensatz befindet. Der Anbieter muss die entsprechende Funktionalität unterstützen, damit diese Eigenschaft verfügbar ist.  
  
 **AbsolutePage** ist 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu wechseln. Abrufen der Gesamtzahl der Seiten aus der **PageCount** -Eigenschaft.
