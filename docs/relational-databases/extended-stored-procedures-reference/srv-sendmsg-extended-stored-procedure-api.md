---
title: srv_sendmsg (API für die erweiterte gespeicherte Prozedur) | Microsoft-Dokumentation
description: Informieren Sie sich über srv_sendmsg in der API für erweiterte gespeicherte Prozeduren und darüber, wie diese eine Nachricht an den Client senden kann.
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: stored-procedures
ms.topic: reference
apiname:
- srv_sendmsg
apilocation:
- opends60.dll
apitype: DLLExport
dev_langs:
- C++
helpviewer_keywords:
- srv_sendmsg
ms.assetid: efcb50b9-f8ff-4121-bf67-05830171b928
author: rothja
ms.author: jroth
ms.openlocfilehash: 3737b6633710a3831cf8cbcb3801263582369dc7
ms.sourcegitcommit: 216f377451e53874718ae1645a2611cdb198808a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2020
ms.locfileid: "87248240"
---
# <a name="srv_sendmsg-extended-stored-procedure-api"></a>srv_sendmsg (API für erweiterte gespeicherte Prozeduren)
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
    
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureDontUse](../../includes/ssnotedepfuturedontuse-md.md)] Verwenden Sie stattdessen die CLR-Integration.  
  
 Sendet eine Meldung an den Client.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
int srv_sendmsg (  
SRV_PROC *  
srvproc  
,  
int  
msgtype  
,  
DBINT  
msgnum  
,  
DBTINYINT  
class  
,   
DBTINYINT  
state  
,  
DBCHAR *  
rpcname  
,  
int   
rpcnamelen  
,  
DBUSMALLINT  
linenum  
,  
DBCHAR *  
message  
,  
int  
msglen   
);  
```  
  
## <a name="arguments"></a>Argumente  
 *srvproc*  
 Ein Zeiger auf die SRV_PROC-Struktur, die das Handle für eine bestimmte Clientverbindung ist (in diesem Fall das Handle, das die Sprachanforderung erhalten hat). Die Struktur enthält Informationen, mit der die API-Bibliothek für erweiterte gespeicherte Prozeduren die Kommunikation und Daten zwischen der Anwendung und dem Client verwaltet.  
  
 *msgtype*  
 Ist entweder SRV_MSG_INFO oder SRV_MSG_ERROR, je nachdem, ob der Server eine Informations- oder Fehlermeldung sendet.  
  
 *msgnum*  
 Eine 4-Byte-Meldungsnummer.  
  
 *class*  
 Gibt den Fehlerschweregrad an. Ein Schweregrad kleiner oder gleich 10 wird als Informationsmeldung betrachtet.  
  
 *state*  
 Stellt die Fehlerzustandsnummer für die aktuelle Meldung bereit. Die Fehlerzustandsnummer enthält Informationen über den Fehlerkontext. Gültige Zustandsnummern liegen zwischen 0 und 255.  
  
 *rpcname*  
 Wird derzeit nicht unterstützt.  
  
 *rpcnamelen*  
 Wird derzeit nicht unterstützt.  
  
 *linenum*  
 Die Zeilennummer im Sprachbefehlsbatch, für die die Meldung gilt. Die Zeilennummern beginnen bei 1. Legen Sie den Wert auf 0 fest, wenn *linenum* nicht für die Meldung gilt.  
  
 *Nachricht*  
 Ein Zeiger auf die an den Client zu sendende Zeichenfolge.  
  
 *msglen*  
 Gibt die Länge von *message*in Byte an. Wenn *message* NULL-terminiert ist, legen Sie für *msglen* den Wert SRV_NULLTERM fest.  
  
## <a name="returns"></a>Gibt zurück  
 SUCCEED oder FAIL  
  
## <a name="remarks"></a>Bemerkungen  
 Diese Funktion sendet Fehler- oder Informationsmeldungen an den Client. Sie wird für jede zu sendende Meldung einmal aufgerufen.  
  
 Mithilfe von **srv_sendmsg** können Meldungen in beliebiger Reihenfolge gesendet werden, bevor oder nachdem alle Zeilen (sofern vorhanden) mit **srv_sendrow**gesendet wurden. Ggf. müssen alle Meldungen an den Client gesendet werden, bevor der Abschlussstatus mit **srv_senddone**gesendet wird.  
  
 Zum Versenden von Meldungen in Unicode verwenden Sie **srv_wsendmsg** anstelle von **srv_sendmsg**.  
  
 Weitere Informationen finden Sie unter [Unicode Data and Server Code Pages (Unicode-Daten und Server Codepages)](../../relational-databases/extended-stored-procedures-programming/unicode-data-and-server-code-pages.md).  
  
> [!IMPORTANT]  
>  Sie sollten den Quellcode der erweiterten gespeicherten Prozeduren sorgfältig prüfen, und Sie sollten die kompilierten DLL-Dateien testen, bevor Sie sie auf einem Produktionsserver installieren. Weitere Informationen zum Überprüfen und Testen der Sicherheit finden Sie auf dieser [Microsoft-Website](https://go.microsoft.com/fwlink/?LinkID=54761&amp;clcid=0x409https://msdn.microsoft.com/security/).  
  
  
