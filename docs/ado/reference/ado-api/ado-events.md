---
description: ADO-Ereignisse
title: ADO-Ereignisse | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: reference
helpviewer_keywords:
- events [ADO]
- ADO, events
ms.assetid: 0ded5ad9-8f83-4224-95af-38512783b972
author: rothja
ms.author: jroth
ms.openlocfilehash: 343d24455490674a9c926d94a902906992679a2c
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99164930"
---
# <a name="ado-events"></a>ADO-Ereignisse

|Ereignis|BESCHREIBUNG|  
|-|-|  
|[BeginTransComplete](./begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md)|Wird nach dem **BeginTrans** -Vorgang aufgerufen.|  
|[CommitTransComplete](./begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md)|Wird nach dem **CommitTrans** -Vorgang aufgerufen.|  
|[ConnectComplete](./connectcomplete-and-disconnect-events-ado.md)|Wird aufgerufen, nachdem eine Verbindung gestartet wurde.|  
|[Disconnect](./connectcomplete-and-disconnect-events-ado.md) (Trennen)|Wird aufgerufen, nachdem eine Verbindung beendet wurde.|  
|[EndOf Recordset](./endofrecordset-event-ado.md)|Wird aufgerufen, wenn versucht wird, zu einer Zeile hinter dem Ende des **Recordsets** zu wechseln.|  
|[ExecuteComplete](./executecomplete-event-ado.md)|Wird aufgerufen, nachdem die Ausführung eines Befehls abgeschlossen wurde.|  
|[FetchComplete](./fetchcomplete-event-ado.md)|Wird aufgerufen, nachdem alle Datensätze in einem langwierigen asynchronen Vorgang in das **Recordset** abgerufen wurden.|  
|[FetchProgress](./fetchprogress-event-ado.md)|Wird in regelmäßigen Abständen während eines langwierigen asynchronen Vorgangs aufgerufen, um zu melden, wie viele Zeilen derzeit in das **Recordset** abgerufen wurden.|  
|[FieldChangeComplete](./willchangefield-and-fieldchangecomplete-events-ado.md)|Wird aufgerufen, nachdem der Wert von einem oder mehreren **Feld** Objekten geändert wurde.|  
|[InfoMessage](./infomessage-event-ado.md)|Wird aufgerufen, wenn während eines **ConnectionEvent** -Vorgangs eine Warnung auftritt.|  
|[Der Vorgang wurde beendet.](./willmove-and-movecomplete-events-ado.md)|Wird aufgerufen, nachdem die aktuelle Position im **Recordset geändert wurde** .|  
|[RecordChangeComplete](./willchangerecord-and-recordchangecomplete-events-ado.md)|Wird aufgerufen, nachdem ein oder mehrere Datensätze geändert wurden.|  
|[RecordsetChangeComplete](./willchangerecordset-and-recordsetchangecomplete-events-ado.md)|Wird aufgerufen, nachdem das **Recordset** geändert wurde.|  
|[RollbackTransComplete](./begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md)|Wird nach dem **RollbackTrans** -Vorgang aufgerufen.|  
|[WillChangeField](./willchangefield-and-fieldchangecomplete-events-ado.md)|Wird aufgerufen, bevor bei einem ausstehenden Vorgang der Wert von einem oder mehreren **Feld** Objekten im **Recordset** geändert wird.|  
|[WillChangeRecord](./willchangerecord-and-recordchangecomplete-events-ado.md)|Wird aufgerufen, bevor ein oder mehrere Datensätze (Zeilen) in der **recordmenge** geändert werden.|  
|[WillChangeRecordset](./willchangerecordset-and-recordsetchangecomplete-events-ado.md)|Wird aufgerufen, bevor das **Recordset** durch einen ausstehenden Vorgang geändert wird.|  
|[WillConnect](./willconnect-event-ado.md)|Wird aufgerufen, bevor eine Verbindung gestartet wird.|  
|[WillExecute](./willexecute-event-ado.md)|Wird aufgerufen, kurz bevor ein ausstehender Befehl für diese Verbindung ausgeführt wird, und bietet dem Benutzer die Möglichkeit, die ausstehenden Ausführungs Parameter zu überprüfen und zu ändern.|  
|[WillMove](./willmove-and-movecomplete-events-ado.md)|Das Ereignis " **WillMove** " wird aufgerufen, *bevor* die aktuelle Position im **Recordset** durch einen ausstehenden Vorgang geändert wird.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [ADO-API-Referenz](./ado-api-reference.md)   
 [ADO-Sammlungen](./ado-collections.md)   
 [Dynamische ADO-Eigenschaften](./ado-dynamic-properties.md)   
 [ADO-Enumerationskonstanten](./ado-enumerated-constants.md)   
 [Anhang B: ADO-Fehler](../../guide/appendixes/appendix-b-ado-errors.md)   
 [Behandeln von ADO-Ereignissen](../../guide/data/handling-ado-events.md)   
 [ADO-Methoden](./ado-methods.md)   
 [ADO-Objektmodell](./ado-object-model.md)   
 [ADO-Objekte und-Schnittstellen](./ado-objects-and-interfaces.md)   
 [ADO-Eigenschaften](./ado-properties.md)