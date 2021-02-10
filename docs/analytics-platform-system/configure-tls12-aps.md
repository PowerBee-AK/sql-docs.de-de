---
title: Konfigurieren von TLS 1,2
description: Empfehlung zum Konfigurieren von TLS 1,2 in APS
author: mzaman1
ms.prod: sql
ms.technology: data-warehouse
ms.topic: conceptual
ms.date: 10/29/2018
ms.author: murshedz
ms.reviewer: martinle
ms.openlocfilehash: 561a0a4f1d45d78e0f2fd23d61aae67f6adb6ff7
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100052741"
---
# <a name="configure-tls-12-in-aps"></a>Konfigurieren von TLS 1,2 in APS

Um APS so zu sichern, dass nur TLS 1,2 verwendet wird, müssen Sie das andere Protokoll auf allen physischen und virtuellen Hosts explizit deaktivieren. Das Deaktivieren von Protokollen erfordert Änderungen an der Registrierungs Einstellung. Registrierungs Änderungen erfordern einen Neustart der virtuellen und physischen Hosts.

> [!WARNING]
> Dieser Abschnitt, diese Methode oder Aufgabe enthält Schritte, die Ihnen zeigen, wie Sie die Registrierung ändern. Schwerwiegende Probleme können jedoch auftreten, wenn Sie die Registrierung falsch ändern, was zu Datenverlusten führen kann und eine Neuinstallation des Betriebssystems erforderlich ist. Es wird dringend empfohlen, die Registrierung zu sichern, bevor Sie Sie ändern. Sie können dann die Registrierung wiederherstellen, falls ein Problem auftritt. Weitere Informationen zum Sichern und Wiederherstellen der Registrierung erhalten Sie, indem Sie auf die folgende Artikelnummer klicken, um den Artikel in der Microsoft Knowledge Base anzuzeigen:<br>
[322756](https://support.microsoft.com/help/322756) sichern und Wiederherstellen der Registrierung in Windows

**Ier**
```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.0]
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.0\Client]
"Enabled"=dword:00000000
"DisabledByDefault"=dword:00000001
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.0\Server]
"Enabled"=dword:00000000
"DisabledByDefault"=dword:00000001
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.1]
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.1\Client]
"Enabled"=dword:00000000
"DisabledByDefault"=dword:00000001
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.1\Server]
"Enabled"=dword:00000000
"DisabledByDefault"=dword:00000001
```

Legen Sie außerdem die folgenden Schlüssel auf den Client Computern fest, auf denen Tools wie APS SSIS-Ziel Adapter installiert sind.
```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\v4.0.30319]
"SystemDefaultTlsVersions"=dword:00000001
"SchUseStrongCrypto"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319]
"SystemDefaultTlsVersions"=dword:00000001
"SchUseStrongCrypto"=dword:00000001 
```



