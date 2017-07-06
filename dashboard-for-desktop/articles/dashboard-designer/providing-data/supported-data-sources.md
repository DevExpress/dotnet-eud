---
title: Supported Data Sources
---
# Supported Data Sources
The Dashboard Designer allows you to establish a connection to various data sources such as SQL databases, Microsoft Excel workbooks, XML/CSV data files or OLAP cubes.

The following data source types are supported.
* [SQL Data Source](#sql-data-source)
* [OLAP Data Source](#olap-data-source)
* [Microsoft Excel Workbooks/CSV Files](#microsoft-excel-workbooks/csv-files)

## <a name="sql-data-source"/>SQL Data Source
To connect to various SQL databases, the Dashboard Designer requires corresponding providers to be installed on the client machine. The table below lists the supported data sources and the required data providers.

| SQL Data Source | Supported Versions | Provider | Database Provider Assembly | Download link |
|---|---|---|---|---|
| Microsoft SQL Server | 2005, 2008, 2008R2, 2012, 2014, 2016, 2005 Express Edition, 2008 R2 Express, 2012 Express, 2014 Express, 2016 Express, Azure SQL Database | .NET Framework Data Provider for SQL Server | System.Data.dll | Included in .NET Framework |
| Microsoft Access | 2000 or higher | Microsoft Jet OLE DB Provider / Microsoft Access Database Engine (ACE) | System.Data.dll | Microsoft Access 2000-2003 - [Microsoft Jet 4.0 Database Engine](https//support.microsoft.com/en-us/kb/239114) / Microsoft Access 2007 and later - [Access Database Engine](https//www.microsoft.com/en-us/download/details.aspx?id=13255) |
| Microsoft SQL Server CE | 3.5, 4.0 | .NET Framework Data Provider for SQL Server Compact | System.Data.SqlServerCe.dll | Included in .NET Framework |
| Oracle Database | 9i or higher | Oracle Data Provider for .NET / .NET Framework Data Provider for Oracle | Oracle.DataAccess.dll, Oracle.ManagedDataAccess.dll, System.Data.OracleClient.dll | [Download link](http//www.oracle.com/technetwork/topics/dotnet/index-085163.html) (Included in .NET Framework) |
| Amazon Redshift | n/a | .NET data provider for PostgreSQL | Npgsql.dll | [Download link](http//www.npgsql.org/) |
| Google BigQuery | n/a | DevExpress.DataAccess.BigQuery ADO.NET provider | DevExpress.DataAccess.BigQuery.dll | [Download link](https//www.nuget.org/packages/devexpress.dataaccess.bigquery) |
| Teradata | 13.0 or higher | .NET Data Provider for Teradata | Teradata.Client.Provider.dll | [Download link](https//downloads.teradata.com/download/connectivity/net-data-provider-for-teradata) |
| SAP Sybase Advantage | Advantage Database Server 9.1 or higher | Advantage .NET Data Provider | Advantage.Data.Provider.dll | [Download link](http//devzone.advantagedatabase.com/dz/content.aspx?key=20&amp;release=19&amp;product=4&amp;platform=11) |
| SAP Sybase ASE | Sybase Adaptive Server 12.0 or higher | SAP Sybase ASE Database Client | Sybase.Data.AseClient.dll | [Download link](http//scn.sap.com/community/developer-center/oltp-db) |
| SAP SQL Anywhere | 11 or higher | SAP SQL Anywhere Database Client | iAnywhere.Data.SQLAnywhere.dll | [Download link](http//scn.sap.com/docs/doc-35857?d96a349c52fc4f68eea46a47ccb3d360) |
| IBM DB2 | 9.5 or higher | ADO.Net client from IBM | IBM.Data.DB2.dll | [Download link](https//www-01.ibm.com/support/docview.wss?rs=4020&amp;uid=swg21385217) |
| Firebird | 1.5 or higher, Dialect 3 | Firebird ADO.NET Data Provider | FirebirdSql.Data.Firebird.dll, FirebirdSql.Data.FirebirdClient.dll | [Download link](http//firebirdsql.org/en/net-provider/) |
| MySQL | 4.1 or higher | ADO.NET driver for MySQL | MySql.Data.dll | [Download link](http//dev.mysql.com/downloads/connector/net/) |
| Pervasive PSQL | 9.x or higher | PSQL ADO.NET Data Provider | Pervasive.Data.SqlClient.dll | [Download link](http//www.pervasive.com/database/home/products/psqlv12.aspx) |
| PostgreSQL | 7.x or higher | .NET data provider for PostgreSQL | Npgsql.dll | [Download link](http//www.npgsql.org/) |
| VistaDB | 4, 5 | VistaDB ADO.NET Provider | VistaDB.5.NET40.dll | [Download link](http//www.gibraltarsoftware.com/vistadb) |
| SQLite | 3.x | ADO.NET provider for SQLite | System.Data.SQLite.dll | [Download link](https//system.data.sqlite.org/index.html/doc/trunk/www/index.wiki) |
| XML file | n/a | n/a | n/a | n/a |

## <a name="olap-data-source"/>OLAP Data Source
To use the OLAP data source, the Dashboard Designer requires Microsoft Analysis Services OLE DB and Microsoft ADOMD.NET providers to be installed on the client machine. To learn more, see [Data providers used for Analysis Services connections](https//msdn.microsoft.com/en-us/library/dn141152.aspx#bkmk_ole).

The following OLAP servers are supported.
* Microsoft SQL Server 2000 Analysis Services
* Microsoft SQL Server 2005 Analysis Services
* Microsoft SQL Server 2008 Analysis Services
* Microsoft SQL Server 2008 R2 Analysis Services
* Microsoft SQL Server 2012 Analysis Services (Multi-dimensional mode)
* Microsoft SQL Server 2014 Analysis Services (Multi-dimensional mode)
* Microsoft SQL Server 2016 Analysis Services (Multi-dimensional mode)

## <a name="microsoft-excel-workbooks/csv-files"/>Microsoft Excel Workbooks/CSV Files
The following Microsoft Excel/text formats are supported.
* XLS
* XLSX
* XLSM
* CSV