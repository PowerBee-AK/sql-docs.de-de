---
description: Einschränkungen der CREATE TABLE-Anweisung
title: Einschränkungen der CREATE TABLE-Anweisung | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- CREATE TABLE statement limitations [ODBC]
- ODBC SQL grammar, CREATE TABLE statement limitations
ms.assetid: c5067855-20c9-456f-8d63-f375b4297f2e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 94b72930fc33c3abbf3920d1290811d0379413c3
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99183189"
---
# <a name="create-table-statement-limitations"></a>Einschränkungen der CREATE TABLE-Anweisung
Wenn Microsoft Access, Microsoft Excel oder paradoxidriver verwendet wird und die Länge einer Text-oder Binary-Spalte nicht angegeben wird (oder als 0 angegeben wird), wird die Spaltenlänge auf 255 festgelegt.  
  
 Wenn der dBase-Treiber verwendet wird und die Länge einer Text-oder Binary-Spalte nicht angegeben wird (oder als 0 angegeben wird), wird die Spaltenlänge auf 254 festgelegt.  
  
 Maximal 255 Spalten werden unterstützt.  
  
 Wenn der Microsoft Excel-Treiber in einer Datenquelle vom Typ "mikrosoftexcel 5,0, 7,0 oder 97" verwendet wird, kann kein Arbeitsblatt mit dem gleichen Namen wie ein zuvor gelöschter Arbeitsblatt erstellt werden. Wenn der Microsoft Excel-Treiber verwendet wird, um auf ein Arbeitsblatt der Version 5,0, 7,0 oder 97 zuzugreifen, löscht eine DROP TABLE-Anweisung das Arbeitsblatt, löscht jedoch nicht den Namen des Arbeitsblatts.  
  
 Wenn der Paradox-Treiber verwendet wird, können Spalten nicht hinzugefügt werden, nachdem ein Index für eine Tabelle definiert wurde. Wenn die erste Spalte der Argumentliste einer CREATE TABLE-Anweisung einen Index erstellt, kann keine zweite Spalte in der Argumentliste enthalten sein.
