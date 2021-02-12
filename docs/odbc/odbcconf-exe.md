---
description: ODBCCONF.EXE
title: ODBCCONF.EXE | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- odbcconf.exe
ms.assetid: 3bf2be83-61f9-4183-836b-85204ac7116a
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: e62fec06a10316bb3b773cf599f11c23ba376cfd
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100075046"
---
# <a name="odbcconfexe"></a>ODBCCONF.EXE
ODBCCONF.exe ist ein Befehlszeilen Tool, mit dem Sie ODBC-Treiber und Datenquellen Namen konfigurieren können.  
  
> [!NOTE]  
>  ODBCCONF.exe werden in einer zukünftigen Version von Windows Data Access Components entfernt. Vermeiden Sie die Verwendung dieser Funktion, und planen Sie das Ändern von Anwendungen, in denen diese Funktion derzeit verwendet wird. Sie können PowerShell-Befehle verwenden, um Treiber und Datenquellen zu verwalten. Weitere Informationen zu diesen PowerShell-Befehlen finden Sie unter [Windows Data Access Components-Cmdlets](/powershell/module/wdac).  
  
## <a name="syntax"></a>Syntax  
  
```console  
ODBCCONF [switches] action  
```  
  
## <a name="arguments"></a>Argumente  
 *Mikro*  
 NULL oder mehr Switch-Optionen. Die Liste der verfügbaren Switches finden Sie im Abschnitt "Hinweise" weiter unten in diesem Thema.  
  
 *action*  
 Eine Aktion, die ausgeführt werden soll. Eine Liste der verfügbaren Optionen finden Sie im Abschnitt "Hinweise".  
  
## <a name="remarks"></a>Bemerkungen  
 Die folgenden Schalter sind verfügbar:  
  
|Schalter|BESCHREIBUNG|  
|------------|-----------------|  
|/A {*Action*}|Geben Sie eine Aktion an.<br /><br /> /A ist optional, wenn nur eine Aktion angegeben wird.|  
|/?|Anzeige der Verwendung für ODBCCONF.EXE.|  
|/C|Die Verarbeitung wird fortgesetzt, wenn eine Aktion fehlschlägt.|  
|/E|Löschen Sie die mit/F angegebene Antwortdatei, wenn die Verarbeitung abgeschlossen ist.|  
|/F|Verwenden Sie eine Antwortdatei, z `odbcconf /F my.rsp` . b..<br /><br /> meine RSP könnte wie folgt aussehen: `REGSVR c:\my.dll`<br /><br /> /A wird in einer Antwortdatei nicht verwendet.|  
|/H|Anzeige Verwendung (Hilfe). Dieser Switch ist mit/? identisch.|  
|/L [*Modus*] *Dateiname*|Senden der Programmausgabe an eine Datei in einem von drei Modi: Normal (n), ausführliche (v) und Debug (d). Im Debugmodus werden die DLLs aufgezeichnet, die von odbcconf.exe geladen werden.<br /><br /> Wenn Sie/L ohne Modus angeben, ist die Protokolldatei leer.<br /><br /> Beispiel: **/LV log.txt**.|  
|/R|Die Aktion wird nach einem Neustart ausgeführt.|  
|/S|Unbeaufsichtigter Modus. Zeigen Sie keine Fehlermeldungen an.|  
  
 Die folgenden Aktionen sind verfügbar:  
  
|Aktion|BESCHREIBUNG|  
|------------|-----------------|  
|ConfigDriver *-driver_name * * Treiber spezifische Konfigurations* Parameter|Lädt die entsprechende Treiber-Setup-DLL und ruft die **ConfigDriver** -Funktion auf.<br /><br /> Entspricht der [sqlconfigdriver-Funktion](../odbc/reference/syntax/sqlconfigdriver-function.md).<br /><br /> Beispiel:<br /><br /> /A {ConfigDriver "Treiber Name" "CPTimeout = 60"}<br /><br /> /A {ConfigDriver "Treiber Name" "driverodbcver = 03.80"}|  
|ConfigDSN *driver_name* DSN =*Name* &#124; *Attribute*|Fügt eine Systemdaten Quelle hinzu oder ändert Sie.<br /><br /> Entspricht der [SQLConfigDataSource-Funktion](../odbc/reference/syntax/sqlconfigdatasource-function.md).<br /><br /> Beispiel:<br /><br /> /A {ConfigDSN "SQL Server" "DSN = Name &#124; Server = SRV"}|  
|Configsysdsn *driver_name* DSN =*Name* &#124; *Attribute*|Fügt eine Systemdaten Quelle hinzu oder ändert Sie.<br /><br /> Entspricht der [SQLConfigDataSource-Funktion](../odbc/reference/syntax/sqlconfigdatasource-function.md).<br /><br /> Beispiel:<br /><br /> /A {configsysdsn "SQL Server" "DSN = Name &#124; Server = SRV"}|  
|InstallDriver|Entspricht der [sqlinstalldriverex-Funktion](../odbc/reference/syntax/sqlinstalldriverex-function.md).<br /><br /> Weitere Informationen zur Syntax der Schlüsselwort-Wert-Paare, die an InstallDriver übermittelt werden, finden Sie [unter Unterschlüssel der Treiber Spezifikation](../odbc/reference/install/driver-specification-subkeys.md)<br /><br /> Beispiel:<br /><br /> /A {InstallDriver "Your Driver &#124; Driver =c:\your.dll &#124; Setup =c:\your.dll &#124; apilevel = 2 &#124; connectfunctions = yyy &#124; driverodbcver = 03.50 &#124; fileusage = 0 &#124; sqllevel = 1"}|  
|Konfiguration des installtranslator- *Konvertierers * * Treiber Pfad*|Fügt dem Registrierungsschlüssel **HKEY_LOCAL_MACHINE\SOFTWARE\ODBC\ODBCINST.INI \ODBC** -Übersetzer Informationen zu einem Konvertierer hinzu.<br /><br /> Entspricht der [sqlinstalltranslatorex-Funktion](../odbc/reference/syntax/sqlinstalltranslatorex-function.md).<br /><br /> Weitere Informationen zur Syntax der Schlüsselwort-Wert-Paare, die an InstallDriver übermittelt werden, finden Sie [unter Übersetzer-Spezifikations](../odbc/reference/install/translator-specification-subkeys.md)<br /><br /> Beispiel:<br /><br /> /A {installtranslator "mein Translator &#124; Translator =c:\my.dll &#124; Setup =c:\my.dll"}|  
|REGSVR- *dll*|Registriert eine DLL.<br /><br /> Entspricht regsvr32.exe.<br /><br /> Beispiel:<br /><br /> /A {REGSVR c:\my.dll}|  
|Setfiledsndir|Wenn HKEY_LOCAL_MACHINE\SOFTWARE\ODBC\ODBC.INI \ODBC-Datei dsn\defaultdsndir nicht vorhanden ist, wird Sie von der setfiledsndir-Aktion erstellt, und ihr wird der Wert in HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\CommonFilesDir zugewiesen, angefügt an \odbc\data sources.<br /><br /> Der Wert unter HKEY_LOCAL_MACHINE\SOFTWARE\ODBC\ODBC.INI \ODBC-Datei dsn\defaultdsndir gibt den Standard Speicherort an, der vom ODBC-Datenquellen-Administrator beim Erstellen einer dateibasierten Datenquelle verwendet wird.<br /><br /> Beispiel:<br /><br /> /A {setfiledsndir}|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Microsoft Open Database Connectivity (ODBC)](../odbc/microsoft-open-database-connectivity-odbc.md)
