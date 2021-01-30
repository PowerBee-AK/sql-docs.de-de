---
description: sp_cursorclose (Transact-SQL)
title: sp_cursorclose (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: reference
f1_keywords:
- sp_cursor_close_TSQL
- sp_cursor_close
dev_langs:
- TSQL
helpviewer_keywords:
- sp_cursorclose
ms.assetid: d9b7b44d-cdff-456e-97df-7031a3b9beb6
author: markingmyname
ms.author: maghan
ms.openlocfilehash: dc19fd9d00cde0bb29582c5bc0079be4039436af
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99205169"
---
# <a name="sp_cursorclose-transact-sql"></a>sp_cursorclose (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Schließt den Cursor und hebt deren Zuordnung auf und gibt alle zugeordneten Ressourcen frei. Das heißt, Sie löscht die temporäre Tabelle, die zur Unterstützung von Keyset oder statischem **Cursor** verwendet wird. sp_cursorclose wird aufgerufen, indem ID = 9 in einem Tabular Data Stream-Paket (TDS) angegeben wird.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
sp_cursorclose cursor  
```  
  
## <a name="arguments"></a>Argumente  
 *Cursor*  
 Ein Cursor *handle* -Wert, der von generiert [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] und von der sp_cursoropen Prozedur zurückgegeben wird. *Cursor* ist ein erforderlicher Parameter, der einen **int** -Eingabe Wert aufruft.  
  
> [!NOTE]  
>  Der Eingabewert -1 gilt für alle Cursor der aktuellen Verbindung.  
  
## <a name="remarks"></a>Bemerkungen  
 der *Cursor* gibt Fehlermeldungen zurück, wenn die Prozedur ausgeführt wurde, nachdem der Cursor geschlossen wurde, oder wenn ein ungültiges Handle angegeben wurde.  
  
 Der RPC-Status gibt an, ob der Vorgang erfolgreich oder fehlerhaft war.  
  
 Die DONE-Zeilenanzahl beträgt immer 0.  
  
## <a name="see-also"></a>Weitere Informationen  
 [sp_cursoropen &#40;Transact-SQL-&#41;](../../relational-databases/system-stored-procedures/sp-cursoropen-transact-sql.md)   
 [Gespeicherte Systemprozeduren &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
