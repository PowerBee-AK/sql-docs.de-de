---
description: Anbieterunterstützung für ADOX (ADO)
title: Anbieter Unterstützung für ADOX (ADO) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- ADOX provider support [ADO]
ms.assetid: 64234ce5-dc46-4c8a-a316-61956b6b9abb
author: rothja
ms.author: jroth
ms.openlocfilehash: 45842fd5035a8b52c68911d29a23a3414a776e02
ms.sourcegitcommit: 917df4ffd22e4a229af7dc481dcce3ebba0aa4d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "100036690"
---
# <a name="provider-support-for-adox-ado"></a>Anbieterunterstützung für ADOX (ADO)
Bestimmte Funktionen von ADOX werden je nach OLE DB Datenanbieter nicht unterstützt. ADOX wird mit dem OLE DB- [Anbieter für Microsoft Jet](../appendixes/microsoft-ole-db-provider-for-microsoft-jet.md)vollständig unterstützt. Die nicht unterstützten Funktionen mit dem [Microsoft OLE DB-Anbieter für SQL Server](../appendixes/microsoft-ole-db-provider-for-sql-server.md), dem [Microsoft OLE DB-Anbieter für ODBC](../appendixes/microsoft-ole-db-provider-for-odbc.md)oder dem [Microsoft OLE DB-Anbieter für Oracle](../appendixes/microsoft-ole-db-provider-for-oracle.md) sind in den folgenden Tabellen aufgeführt. ADOX wird von keinem anderen Anbieter von Microsoft OLE DB unterstützt.  
  
## <a name="microsoft-ole-db-provider-for-sql-server"></a>Microsoft OLE DB-Anbieter für SQL Server  
  
|Objekt oder Sammlung|Verwendungs Einschränkung|  
|--------------------------|-----------------------|  
|**Tabellen** Sammlung|Eigenschaften sind vor der Objekt Erstellung Lese-/Schreibzugriff und schreibgeschützt, wenn auf ein vorhandenes Objekt verwiesen wird.|  
|**Views** -Auflistung|**Sichten** werden nicht unterstützt.|  
|**Prozeduren**|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Procedure** -Objekt|Die **Command** -Eigenschaft wird nicht unterstützt.|  
|**Schlüssel** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Benutzer** Sammlung|**Benutzer** werden nicht unterstützt.|  
|**Groups** -Sammlung|**Gruppen** werden nicht unterstützt.|  
  
## <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB-Anbieter für ODBC  
  
|Objekt oder Sammlung|Verwendungs Einschränkung|  
|--------------------------|-----------------------|  
|**Catalog** -Objekt|Die **Create** -Methode wird nicht unterstützt.|  
|**Tabellen** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt. Eigenschaften sind vor der Objekt Erstellung Lese-/Schreibzugriff und schreibgeschützt, wenn auf ein vorhandenes Objekt verwiesen wird.|  
|**Prozeduren**|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Procedure** -Objekt|Die **Command** -Eigenschaft wird nicht unterstützt.|  
|**Index** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Schlüssel** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Benutzer** Sammlung|**Benutzer** werden nicht unterstützt.|  
|**Groups** -Sammlung|**Gruppen** werden nicht unterstützt.|  
  
## <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB-Anbieter für Oracle  
  
|Objekt oder Sammlung|Verwendungs Einschränkung|  
|--------------------------|-----------------------|  
|**Catalog** -Objekt|Die **Create** -Methode wird nicht unterstützt.|  
|**Tabellen** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt. Eigenschaften sind vor der Objekt Erstellung Lese-/Schreibzugriff und schreibgeschützt, wenn auf ein vorhandenes Objekt verwiesen wird.|  
|**Views** -Auflistung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|Objekt **anzeigen**|Die **Command** -Eigenschaft wird nicht unterstützt.|  
|**Procedures** -Objekt|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Procedure** -Objekt|Die **Command** -Eigenschaft wird nicht unterstützt.|  
|**Index** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Schlüssel** Sammlung|Die **Append** -und **Delete** -Methoden werden nicht unterstützt.|  
|**Benutzer** Sammlung|**Benutzer** werden nicht unterstützt.|  
|**Groups** -Sammlung|**Gruppen** werden nicht unterstützt.|