---
description: MSSQLSERVER_33081
title: MSSQLSERVER_33081 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: reference
helpviewer_keywords:
- 33081 (Database Engine error)
ms.assetid: 839705e7-fa37-4c0d-9f3f-95a9eab98bcf
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 8be9f2bec59b51f75a7832768663535175946f60
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99208419"
---
# <a name="mssqlserver_33081"></a>MSSQLSERVER_33081
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Details  
  
| attribute | Wert |  
| :-------- | :---- |  
|Produktname|SQL Server|  
|Ereignis-ID|33081|  
|Ereignisquelle|MSSQLSERVER|  
|Komponente|SQLEngine|  
|Symbolischer Name|SEC_DLL_TRUST_VERIFICATION_FAILED|  
|Meldungstext|Fehler beim Laden des Kryptografieanbieters ‚%.*ls’ aufgrund einer ungültigen Authenticode-Signatur oder eines ungültigen Dateipfades.  Überprüfen Sie vorhergehende Meldungen auf weitere Fehler.|  
  
## <a name="explanation"></a>Erklärung  
[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] konnte den in der Fehlermeldung aufgeführten Kryptografieanbieter nicht laden. Es sind mehrere Win API-Fehler aufgetreten, die diesen Fehler möglicherweise verursachen. Der Ringpuffer enthält den Namen der fehlerhaften API und den von der API zurückgegebenen Windows-Fehlercode. Weitere Informationen erhalten Sie, indem Sie die folgende Abfrage der sys.dm_os_ring_buffers-Sicht ausgeben.  
  
```  
SELECT * FROM sys.dm_os_ring_buffers   
WHERE ring_buffer_type = 'RING_BUFFER_SECURITY_ERROR';  
```  
  
## <a name="user-action"></a>Benutzeraktion  
Suchen Sie den Windows-Fehlercode in MSDN (https://msdn.microsoft.com/) ), um das Problem zu analysieren. Beheben Sie den Fehler, oder wenden Sie sich an [!INCLUDE[msCoName](../../includes/msconame-md.md)]-CSS für weitere Informationen. Wenn Sie CSS in Anspruch nehmen möchten, halten Sie bitte die folgenden Informationen für unsere Supportmitarbeiter bereit.  
  
-   Das Fehlerprotokoll, das die Meldung über den Fehler beim Laden des Kryptografieanbieters beinhaltet.  
  
-   Die Ausgabe der folgenden Anweisung:  
  
    ```  
    SELECT * FROM sys.dm_os_ring_buffers   
    WHERE ring_buffer_type = 'RING_BUFFER_SECURITY_ERROR';  
    ```  
  
> [!NOTE]  
> Versuchen Sie, die Ringpufferinformationen möglichst umgehend zu erfassen, da Ringpufferinformationen während eines Neustarts verloren gehen können.  
  
