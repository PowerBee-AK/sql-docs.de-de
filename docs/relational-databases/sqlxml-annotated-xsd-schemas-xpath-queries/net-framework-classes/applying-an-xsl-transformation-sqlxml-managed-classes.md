---
title: Anwenden einer XSL-Transformation (SQLXML)
description: Sehen Sie sich ein Beispiel für eine SQL-Abfrage an, die eine XSL-Transformation mithilfe der XslPath-Eigenschaft des SqlXmlCommand-Objekts in den verwalteten SQLXML-Klassen anwendet.
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: xml
ms.topic: reference
helpviewer_keywords:
- applying XSL transformations [SQLXML]
- Managed Classes [SQLXML], applying XSL transformations
- SQLXML Managed Classes, applying XSL transformations
- XSL Transformations [SQLXML]
ms.assetid: 8562043b-3e9f-41a3-bb41-92b9f14363c4
author: MightyPen
ms.author: genemi
ms.custom: seo-lt-2019
monikerRange: =azuresqldb-current||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: 03b33945a727cd7010800c9d78254733fb9f2d7e
ms.sourcegitcommit: 1a544cf4dd2720b124c3697d1e62ae7741db757c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "97414581"
---
# <a name="applying-an-xsl-transformation-sqlxml-managed-classes"></a>Anwenden einer XSL-Transformation (Verwaltete SQLXML-Klassen)
[!INCLUDE [SQL Server Azure SQL Database](../../../includes/applies-to-version/sql-asdb.md)]
  In diesem Beispiel wird eine SQL-Abfrage der AdventureWorks-Datenbank ausgeführt. Die XSL-Transformation wird auf das Abfrageergebnis angewendet, um eine zweispaltige Tabelle mit den Vor- und Nachnamen der Mitarbeiter zu generieren.  
  
 Die XslPath-Eigenschaft des SqlXmlCommand-Objekts wird verwendet, um die XSL-Datei und ihren Verzeichnispfad anzugeben.  
  
> [!NOTE]  
>  Im Code müssen Sie den Namen der Instanz von Microsoft [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] in der Verbindungszeichenfolge bereitstellen.  
  
```  
using System;  
using Microsoft.Data.SqlXml;  
using System.IO;  
class Test  
{  
      static string ConnString = "Provider=SQLOLEDB;Server=(local);database=AdventureWorks;Integrated Security=SSPI";  
      public static int testXSL()  
      {  
         //Stream strm;  
         SqlXmlCommand cmd = new SqlXmlCommand(ConnString);  
         cmd.CommandText = "SELECT TOP 20 FirstName, LastName FROM Person.Contact FOR XML AUTO";  
         cmd.XslPath = "MyXSL.xsl";  
         cmd.RootTag = "root";  
         using (Stream strm = cmd.ExecuteStream()){  
            using (StreamReader sr = new StreamReader(strm)){  
               Console.WriteLine(sr.ReadToEnd());  
            }  
        }  
         return 0;  
      }  
      public static int Main(String[] args)  
      {  
         testXSL();     
         return 0;  
      }  
   }  
```  
  
 Dies ist das XSL-Stylesheet, das Sie verwenden können, um die Anwendung zu testen:  
  
```  
<?xml version='1.0' encoding='UTF-8'?>  
 <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">   
    <xsl:output method="html"/>  
    <xsl:template match = '*'>  
        <xsl:apply-templates />  
    </xsl:template>  
    <xsl:template match = 'Person.Contact'>  
       <TR>  
         <TD><xsl:value-of select = '@FirstName' /></TD>  
         <TD><B><xsl:value-of select = '@LastName' /></B></TD>  
       </TR>  
    </xsl:template>  
    <xsl:template match = '/'>  
      <HTML>  
        <HEAD>  
           <STYLE>th { background-color: #CCCCCC }</STYLE>  
        </HEAD>  
        <BODY>  
         <TABLE border='1' style='width:300;'>  
           <TR><TH colspan='2'>Contacts</TH></TR>  
           <TR><TH >First name</TH><TH>Last name</TH></TR>  
           <xsl:apply-templates select = 'root' />  
         </TABLE>  
        </BODY>  
      </HTML>  
    </xsl:template>  
</xsl:stylesheet>  
```  
  
 Um das Beispiel zu testen, muss auf dem Computer [!INCLUDE[msCoName](../../../includes/msconame-md.md)] .NET Framework installiert sein.  
  
### <a name="to-test-the-application"></a>So testen Sie die Anwendung  
  
1.  Speichern Sie das XSL-Stylesheet in einer Datei (MyXSL.xsl).  
  
2.  Speichern Sie den C#-Code (DocSample.cs) aus dem Beispiel im selben Ordner, in dem das Stylesheet gespeichert ist.  
  
3.  Kompilieren Sie den Code. Verwenden Sie zur Kompilierung des Codes an der Eingabeaufforderung die folgende Zeichenfolge:  
  
    ```  
    csc /reference:Microsoft.Data.SqlXML.dll DocSample.cs  
    ```  
  
     Dadurch wird eine ausführbare Datei (DocSample.exe) erstellt.  
  
4.  Führen Sie DocSample.exe an der Eingabeaufforderung aus.  

## <a name="applying-an-xsl-transformation-in-the-net-framework"></a>Anwenden einer XSL-Transformation in .NET Framework  
 Anstatt eine XSL-Transformation auf der mittleren Ebene anzuwenden, wie zuvor beschrieben, können Sie sie auf der Clientebene anwenden (.NET Framework). Der folgende überarbeitete C#-Code zeigt, wie die XSL-Transformation in .NET Framework angewendet wird.  
  
> [!NOTE]  
>  Im Code müssen Sie den Namen der Instanz von [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] in der Verbindungszeichenfolge bereitstellen.  
  
```  
using System;  
using System.Xml;  
using Microsoft.Data.SqlXml;  
using System.IO;  
using System.Xml.XPath;  
using System.Xml.Xsl;  
  
class Test  
{  
      static string ConnString = "Provider=SQLOLEDB;Server=(local);database=AdventureWorks;Integrated Security=SSPI";  
      public static int testXSL()  
      {  
         //Stream strm;  
         SqlXmlCommand cmd = new SqlXmlCommand(ConnString);  
         cmd.CommandText = "SELECT TOP 20 FirstName, LastName FROM Person.Contact FOR XML AUTO";  
         cmd.RootTag = "root";  
         using (Stream strm = cmd.ExecuteStream()){  
            XmlReader reader = new XmlReader(strm);  
            XPathDocument xd = new XPathDocument(reader, XmlSpace.Preserve);  
            XslCompiledTransform xslt = new XslCompiledTransform();  
            xslt.Load("MyXSL.xsl");  
            XmlWriter writer = XmlWriter.Create("xslt_output.html");  
            xslt.Transform(xd, writer);  
            reader.Close();  
            writer.Close();  
         }  
         return 0;  
      }  
      public static int Main(String[] args)  
      {  
         testXSL();     
         return 0;  
      }  
   }  
```  
  
  
