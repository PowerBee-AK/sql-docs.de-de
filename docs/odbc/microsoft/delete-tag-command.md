---
description: DELETE TAG-Befehl
title: Befehl zum Löschen von Tags | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
helpviewer_keywords:
- DELETE TAG command [ODBC]
ms.assetid: 4f4e1362-a5f3-4b15-8a3c-d4e96605f221
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: aa431c50fcd151d57ce7613586587a1c2342a5c7
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99181563"
---
# <a name="delete-tag-command"></a>DELETE TAG-Befehl
Entfernt ein Tag oder Tags aus einer Verbund Indexdatei (. CDX).  
  
## <a name="syntax"></a>Syntax  
  
```  
  
DELETE TAG TagName1 [OF CDXFileName1]  
   [, TagName2 [OF CDXFileName2]] ...  
  Or   
DELETE TAG ALL [OF CDXFileName]  
```  
  
## <a name="arguments"></a>Argumente  
 *TagName1* Of *CDXFileName1*[, *TagName2*[of *CDXFileName2*]]...  
 Gibt ein Tag an, das aus einer Verbund Indexdatei entfernt werden soll. Sie können mehrere Tags mit einem DELETE-Tag löschen, indem Sie eine Liste von Tagnamen einschließen, die durch Kommas getrennt sind. Wenn zwei oder mehr Tags mit dem gleichen Namen in den geöffneten Indexdateien vorhanden sind, können Sie ein Tag aus einer bestimmten Indexdatei entfernen, indem Sie *cdxfilename* einschließen.  
  
 Alle [von *cdxfilename*]  
 Entfernt jedes Tag aus einer Verbund Indexdatei. Wenn die aktuelle Tabelle über eine Struktur zusammengesetzte Indexdatei verfügt, werden alle Tags aus der Indexdatei entfernt, die Indexdatei wird vom Datenträger gelöscht, und das-Flag im Header der Tabelle, das angibt, dass eine zugeordnete Struktur zusammengesetzter Indexdatei entfernt wird. Verwenden Sie all with von *cdxfilename* , um alle Tags aus einer geöffneten Verbund Indexdatei zu entfernen, die nicht die Struktur der zusammengesetzten Indizes ist.  
  
## <a name="remarks"></a>Bemerkungen  
 Zusammengesetzte Indexdateien, die mit Index erstellt wurden, enthalten Tags, die den Indexeinträgen entsprechen. Das Tag "Delete" wird verwendet, um ein Tag oder Tags aus geöffneten Verbund Indexdateien zu entfernen. Sie können nur Tags aus Verbund Indexdateien löschen, die im aktuellen Arbeitsbereich geöffnet sind. Wenn Sie alle Tags aus einer Verbund Indexdatei entfernen, wird die Datei vom Datenträger gelöscht.  
  
 Visual FoxPro sucht zuerst nach einem Tag in der Struktur der zusammengesetzten Indexdatei (sofern eine solche geöffnet ist). Wenn das-Tag nicht in der Struktur der zusammengesetzten Indexdatei ist, sucht Visual FoxPro in den anderen geöffneten Verbund Indexdateien nach dem-Tag.  
  
## <a name="see-also"></a>Weitere Informationen  
 [INDEX-Befehl](../../odbc/microsoft/index-command.md)
