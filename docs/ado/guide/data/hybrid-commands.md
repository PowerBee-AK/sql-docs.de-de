---
description: Hybridbefehle
title: Hybrid Befehle | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- shape commands [ADO]
- hybrid commands [ADO]
- data shaping [ADO], hybrid commands
ms.assetid: e8ca40e8-459c-40e2-8dd3-3ec6d5ee7b51
author: rothja
ms.author: jroth
ms.openlocfilehash: e3ac822fef8270649240e18fc9bc061203c88bb1
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100032762"
---
# <a name="hybrid-commands"></a>Hybridbefehle
Hybrid Befehle sind teilweise parametrisierte Befehle. Beispiel:  
  
```  
SHAPE {select * from plants}   
   APPEND( {select * from customers where country = ?}   
           RELATE PlantCountry TO PARAMETER 0,   
             PlantRegion TO CustomerRegion )   
```  
  
 Das zwischen Speicherungs Verhalten für einen Hybriden Befehl ist identisch mit dem von regulären parametrisierten Befehlen.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Beispiel für Daten Strukturierung](./data-shaping-example.md)   
 [Formale Form Grammatik](./formal-shape-grammar.md)   
 [Shape-Befehle im Allgemeinen](./shape-commands-in-general.md)