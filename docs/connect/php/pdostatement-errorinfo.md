---
title: PDOStatement::errorInfo
description: API-Referenz für die PDOStatement::errorInfo-Funktion im Microsoft PDO_SQLSRV-Treiber für PHP für SQL Server.
ms.custom: ''
ms.date: 01/29/2021
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
ms.assetid: e45bebe8-ea4c-49b6-93db-cf1ae65f530c
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0474b0c1225a248b47f0892ac940f2e58ab0efa0
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99206354"
---
# <a name="pdostatementerrorinfo"></a>PDOStatement::errorInfo
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

Ruft erweiterte Fehlerinformationen des zuletzt ausgeführten Vorgangs des Anweisungshandles ab  
  
## <a name="syntax"></a>Syntax  

```
array PDOStatement::errorInfo();
```
  
## <a name="return-value"></a>Rückgabewert  
Ein Array mit Fehlerinformationen über den zuletzt ausgeführten Vorgang des Anweisungshandles Dieses Array besteht aus den folgenden Feldern:  
  
-   Der SQLSTATE-Fehlercode  
  
-   Der treiberspezifische Fehlercode  
  
-   Die treiberspezifische Fehlermeldung  
  
Wenn kein Fehler vorliegt oder wenn der SQLSTATE nicht festgelegt ist, werden die treiberspezifischen Felder NULL sein.  
  
## <a name="remarks"></a>Bemerkungen  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../../includes/ssdriverphp_md.md)]hinzugefügt.  
  
## <a name="example"></a>Beispiel  
In diesem Beispiel ist in der SQL-Anweisung ein Fehler aufgetreten, der dann gemeldet wird.  
  
```php
<?php  
$conn = new PDO( "sqlsrv:server=(local) ; Database = AdventureWorks", "", "");  
$stmt = $conn->prepare('SELECT * FROM Person.Addressx');  
  
$stmt->execute();  
print_r ($stmt->errorInfo());  
?>  
```

## <a name="additional-odbc-messages"></a>Weitere ODBC-Meldungen

Wenn eine Ausnahme auftritt, gibt der ODBC-Treiber möglicherweise mehr als einen Fehler zurück, um Sie bei der Problemdiagnose zu unterstützen. PDOStatement::errorInfo zeigt jedoch immer den ersten Fehler an. Als Reaktion auf diesen [Fehlerbericht](https://bugs.php.net/bug.php?id=78196) wurden [PDO::errorInfo](https://www.php.net/manual/en/pdo.errorinfo.php) und [PDOStatement::errorInfo](https://www.php.net/manual/en/pdostatement.errorinfo.php) aktualisiert, um darauf hinzuweisen, dass Treiber *mindestens* die folgenden drei Felder zeigen sollten:
```
0   SQLSTATE error code (a five characters alphanumeric identifier defined in the ANSI SQL standard).
1   Driver specific error code.
2   Driver specific error message.
```

Ab Version 5.9.0 besteht das Standardverhalten von PDOStatement::errorInfo darin, weitere ODBC-Fehler anzuzeigen, sofern Fehler vorliegen. Unter [PDO::errorInfo](../../connect/php/pdo-errorinfo.md) finden Sie weitere Informationen.
  
## <a name="see-also"></a>Weitere Informationen  
[PDOStatement-Klasse](../../connect/php/pdostatement-class.md)

[PDO::errorInfo](../../connect/php/pdo-errorinfo.md)

[PDO](https://php.net/manual/book.pdo.php)  
  
