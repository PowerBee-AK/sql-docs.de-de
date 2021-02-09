---
title: API für das Massenkopieren für Batcheinfügevorgänge in JDBC
description: Der Microsoft JDBC-Treiber für SQL Server unterstützt die Verwendung der Massenkopierfunktion für Batcheinfügevorgänge, damit Daten schneller in die Datenbank geladen werden können.
ms.custom: ''
ms.date: 01/29/2021
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: ''
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 4a769d73f799b8ca0b4b806a3e656517377e23ad
ms.sourcegitcommit: 33f0f190f962059826e002be165a2bef4f9e350c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "99161571"
---
# <a name="using-bulk-copy-api-for-batch-insert-operation"></a>Verwenden der Massenkopierungs-API für den Batcheinfügungsvorgang

[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

Der Microsoft JDBC-Treiber 9.2 für SQL Server unterstützt die API für das Massenkopieren für Batcheinfügevorgänge. Mit diesem Feature können Benutzer dem Treiber bei der Ausführung von Batcheinfügevorgängen das Massenkopieren im Hintergrund ermöglichen. Der Treiber strebt beim Einfügen derselben Daten eine bessere Leistung an, als der Treiber bei einem regulären Batcheinfügevorgang erzielen könnte. Der Treiber analysiert die SQL-Abfrage des Benutzers und nutzt anstelle des üblichen Batcheinfügevorgangs die API für das Massenkopieren. Nachfolgend werden die verschiedenen Möglichkeiten zum Aktivieren der API für das Massenkopieren für Batcheinfügevorgänge sowie die geltenden Einschränkungen aufgeführt. Diese Seite enthält außerdem ein kleines Codebeispiel, das eine Verwendung und die Leistungssteigerung veranschaulicht.

Dieses Feature ist nur auf die `executeBatch()` & `executeLargeBatch()`-APIs von PreparedStatement und CallableStatement anwendbar.

## <a name="prerequisites"></a>Voraussetzungen

Voraussetzung für die Aktivierung der API für das Massenkopieren für Batcheinfügevorgänge

* Die Abfrage muss eine Einfügeabfrage sein (die Abfrage darf Kommentare enthalten, aber muss mit dem INSERT-Schlüsselwort beginnen, damit dieses Feature wirksam ist).

## <a name="enabling-bulk-copy-api-for-batch-insert"></a>Aktivieren der API für das Massenkopieren für Batcheinfügevorgänge

Es gibt drei Möglichkeiten, die API für das Massenkopieren für Batcheinfügevorgänge zu aktivieren.

### <a name="1-enabling-with-connection-property"></a>1. Aktivierung mit der Verbindungseigenschaft

Durch das Hinzufügen von **useBulkCopyForBatchInsert=true;** zur Verbindungszeichenfolge wird dieses Feature aktiviert.

```java
Connection connection = DriverManager.getConnection("jdbc:sqlserver://<server>:<port>;userName=<user>;password=<password>;database=<database>;useBulkCopyForBatchInsert=true;");
```

### <a name="2-enabling-with-setusebulkcopyforbatchinsert-method-from-sqlserverconnection-object"></a>2. Aktivierung mit der setUseBulkCopyForBatchInsert()-Methode aus dem SQLServerConnection-Objekt

Durch den Aufruf von **SQLServerConnection.setUseBulkCopyForBatchInsert(true)** wird dieses Feature aktiviert.

**SQLServerConnection.getUseBulkCopyForBatchInsert()** ruft den aktuellen Wert für die Verbindungseigenschaft **useBulkCopyForBatchInsert** ab.

Der Wert für **useBulkCopyForBatchInsert** bleibt für jede PreparedStatement zum Zeitpunkt der Initialisierung konstant. Alle nachfolgenden Aufrufe von **SQLServerConnection.setUseBulkCopyForBatchInsert()** haben keine Auswirkung auf den Wert der bereits erstellten PreparedStatement-Objekts.

### <a name="3-enabling-with-setusebulkcopyforbatchinsert-method-from-sqlserverdatasource-object"></a>3. Aktivierung mit der setUseBulkCopyForBatchInsert()-Methode aus dem SQLServerDataSource-Objekt

Ähnlich wie oben, aber es wird SQLServerDataSource verwendet, um ein SQLServerConnection-Objekt zu erstellen. Mit beiden Methoden werden die gleichen Ergebnisse erzielt.

## <a name="known-limitations"></a>Bekannte Einschränkungen

Für dieses Feature gelten aktuell die folgenden Einschränkungen.

* Einfügeabfragen, die nicht parametrisierte Werte enthalten (z. B. `INSERT INTO TABLE VALUES (?, 2`), werden nicht unterstützt. Platzhalter (?) sind die einzigen unterstützten Parameter für diese Funktion.
* Einfügeabfragen, die INSERT-SELECT-Ausdrücke enthalten (z. B. `INSERT INTO TABLE SELECT * FROM TABLE2`), werden nicht unterstützt.
* Einfügeabfragen, die mehrere VALUE-Ausdrücke enthalten (z. B. `INSERT INTO TABLE VALUES (1, 2) (3, 4)`), werden nicht unterstützt.
* Einfügeabfragen, auf die eine OPTION-Klausel und mehrere Tabellen oder eine andere Abfrage folgt, werden nicht unterstützt.
* Aufgrund der Einschränkungen der API für das Massenkopieren werden die Datentypen `MONEY`, `SMALLMONEY`, `DATE`, `DATETIME`, `DATETIMEOFFSET`, `SMALLDATETIME`, `TIME`, `GEOMETRY` und `GEOGRAPHY` für dieses Feature aktuell nicht unterstützt.

Wenn die Abfrage aufgrund eines nicht SQL Server-bezogenen Fehlers nicht ausgeführt werden kann, protokolliert der Treiber die Fehlermeldung und verwendet die ursprüngliche Logik für Batcheinfügevorgänge.

## <a name="example"></a>Beispiel

Das nachfolgende Beispiel veranschaulicht einen Anwendungsfall für einen Batcheinfügevorgang mit tausend Zeilen für beide Szenarios (regulär im Vergleich zur API für das Massenkopieren).

```java
    public static void main(String[] args) throws Exception
    {
        String tableName = "batchTest";
        String tableNameBulkCopyAPI = "batchTestBulk";

        String connectionUrl = "jdbc:sqlserver://<server>:<port>;databaseName=<database>;user=<user>;password=<password>";

        try (Connection con = DriverManager.getConnection(connectionUrl);
                Statement stmt = con.createStatement();
                PreparedStatement pstmt = con.prepareStatement("insert into " + tableName + " values (?, ?)");) {

            String dropSql = "if exists (select * from dbo.sysobjects where id = object_id(N'[dbo].[" + tableName + "]') and OBJECTPROPERTY(id, N'IsUserTable') = 1) DROP TABLE [" + tableName + "]";
            stmt.execute(dropSql);

            String createSql = "create table " + tableName + " (c1 int, c2 varchar(20))";
            stmt.execute(createSql);

            System.out.println("Starting batch operation using regular batch insert operation.");
            long start = System.currentTimeMillis();
            for (int i = 0; i < 1000; i++) {
                pstmt.setInt(1, i);
                pstmt.setString(2, "test" + i);
                pstmt.addBatch();
            }
            pstmt.executeBatch();

            long end = System.currentTimeMillis();

            System.out.println("Finished. Time taken : " + (end - start) + " milliseconds.");
        }

        try (Connection con = DriverManager.getConnection(connectionUrl + ";useBulkCopyForBatchInsert=true");
                Statement stmt = con.createStatement();
                PreparedStatement pstmt = con.prepareStatement("insert into " + tableNameBulkCopyAPI + " values (?, ?)");) {

            String dropSql = "if exists (select * from dbo.sysobjects where id = object_id(N'[dbo].[" + tableNameBulkCopyAPI + "]') and OBJECTPROPERTY(id, N'IsUserTable') = 1) DROP TABLE [" + tableNameBulkCopyAPI + "]";
            stmt.execute(dropSql);

            String createSql = "create table " + tableNameBulkCopyAPI + " (c1 int, c2 varchar(20))";
            stmt.execute(createSql);

            System.out.println("Starting batch operation using Bulk Copy API.");
            long start = System.currentTimeMillis();
            for (int i = 0; i < 1000; i++) {
                pstmt.setInt(1, i);
                pstmt.setString(2, "test" + i);
                pstmt.addBatch();
            }
            pstmt.executeBatch();

            long end = System.currentTimeMillis();

            System.out.println("Finished. Time taken : " + (end - start) + " milliseconds.");
        }
    }
```

Ergebnis:

```bash
Starting batch operation using regular batch insert operation.
Finished. Time taken : 104132 milliseconds.
Starting batch operation using Bulk Copy API.
Finished. Time taken : 1058 milliseconds.
```

## <a name="see-also"></a>Weitere Informationen

[Verbessern von Leistung und Zuverlässigkeit mit dem JDBC-Treiber](improving-performance-and-reliability-with-the-jdbc-driver.md)
