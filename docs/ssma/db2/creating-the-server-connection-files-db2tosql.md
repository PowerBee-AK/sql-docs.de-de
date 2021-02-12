---
description: Erstellen der Server Verbindungs Dateien (DB2ToSQL)
title: Erstellen der Server Verbindungs Dateien (DB2ToSQL) | Microsoft-Dokumentation
ms.prod: sql
ms.custom: ''
ms.date: 07/14/2020
ms.reviewer: ''
ms.technology: ssma
ms.topic: conceptual
ms.assetid: 685419f6-8606-462c-be12-8bace45bede6
author: nahk-ivanov
ms.author: alexiva
ms.openlocfilehash: 6a03c33bac6415ed4916b5bf7d95cfcff38183be
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100076643"
---
# <a name="creating-the-server-connection-files-db2tosql"></a>Erstellen der Server Verbindungs Dateien (DB2ToSQL)

Server Informationen können entweder im Abschnitt Server der Skriptdatei oder in einer separaten Server Verbindungs Datei angegeben werden. Der Befehlszeilenparameter für die Server Verbindungs Datei ist, `-c <serverconnectionfile>` . Wenn dieselbe Server-ID sowohl in der Skriptdatei als auch in der Server Verbindungs Datei vorhanden ist, wird die Server Definition in der Skriptdatei berücksichtigt.

**Beispiel: 1**

```xml
<!-- Sample of server connection file commands -->
<db2 name="<source-server-unique-name>">
  <standard-mode>

    <connection-provider value="OleDB Provider" />

    <!-- Defines server manager to connect.
         Available manager attribute values
           • zOs - DB2 for z/OS
           • LUW - DB2 for Linux, Unix and Windows
           • DBi - DB2 for i -->
    <database-manager value="$Db2Manager$" />

    <server-name value="$Db2HostName$" />

    <port value="$Db2Port$" />

    <initial-catalog value="$Db2Instance$" />

    <user-id value="$Db2UserName$" />

    <password value="$Db2Password$"/>

  </standard-mode>
</db2>
```

```xml
<sql-server name="<target-server-unique-name>">
  <sql-server-authentication>

    <server value="<server-name>" />

    <database value="<database-name>" />
  
    <user-id value="<user-name>"/>
  
    <password value="<password>"/>

  </sql-server-authentication>
</sql-server>
```

## <a name="next-step"></a>Nächster Schritt

Der nächste Schritt beim Betrieb der Konsole ist [die Ausführung der SSMA-Konsole &#40;DB2ToSQL&#41;](../../ssma/db2/executing-the-ssma-console-db2tosql.md)

## <a name="see-also"></a>Weitere Informationen

- [Ausführen der SSMA-Konsole](./executing-the-ssma-console-db2tosql.md)