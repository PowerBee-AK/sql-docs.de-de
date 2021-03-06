---
title: Benutzerdefinierte CLR-Funktionen | Microsoft-Dokumentation
description: SQL Server CLR-Integration ermöglicht es Ihnen, benutzerdefinierte Skalarwertfunktionen, Tabellenwert Funktionen und Aggregatfunktionen in jeder .NET Framework Programmiersprache zu erstellen.
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: clr
ms.topic: reference
helpviewer_keywords:
- building database objects [CLR integration], user-defined functions
- functions [CLR integration]
- common language runtime [SQL Server], user-defined functions
- database objects [CLR integration], user-defined functions
- user-defined functions [CLR integration]
ms.assetid: 6f7491f1-9a46-4146-ae09-056248634de2
author: rothja
ms.author: jroth
ms.openlocfilehash: fe481b1a49f8eba69bbf913e49f398c86244b952
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "85727856"
---
# <a name="clr-user-defined-functions"></a>CLR-benutzerdefinierte Funktionen
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  Benutzerdefinierte Funktionen sind Routinen, die Parameter annehmen, Berechnungen oder andere Aktionen ausführen und Ergebnisse zurückgeben können. Ab [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] können Sie benutzerdefinierte Funktionen in jeder beliebigen [!INCLUDE[msCoName](../../includes/msconame-md.md)] .NET Framework-Programmiersprache schreiben, beispielsweise in [!INCLUDE[msCoName](../../includes/msconame-md.md)] Visual Basic .NET oder [!INCLUDE[msCoName](../../includes/msconame-md.md)] Visual C#.  
  
 Es sind zwei Arten von Funktionen verfügbar: Skalarfunktionen, die einen einzigen Wert zurückgeben, und Tabellenwertfunktionen, die einen Satz Zeilen zurückgeben.  
  
 In der folgenden Tabelle sind die Themen dieses Abschnitts aufgeführt.  
  
 [CLR-Skalarwertfunktionen](../../relational-databases/clr-integration-database-objects-user-defined-functions/clr-scalar-valued-functions.md)  
 Beschreibt Implementierungsanforderungen und führt Beispiele für Skalarwertfunktionen an.  
  
 [CLR-Tabellenwertfunktionen](../../relational-databases/clr-integration-database-objects-user-defined-functions/clr-table-valued-functions.md)  
 Erörtert, wie Tabellenwertfunktionen (Table-Valued Functions, TVFs) implementiert und verwendet werden, und beschreibt die Unterschiede zwischen [!INCLUDE[tsql](../../includes/tsql-md.md)]- und CLR-TVFs.  
  
 [Benutzerdefinierte CLR-Aggregate](../../relational-databases/clr-integration-database-objects-user-defined-functions/clr-user-defined-aggregates.md)  
 Beschreibt die Implementierung und Verwendung von benutzerdefinierten Aggregaten.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Benutzerdefinierte Funktionen](../../relational-databases/user-defined-functions/user-defined-functions.md)  
  
  
