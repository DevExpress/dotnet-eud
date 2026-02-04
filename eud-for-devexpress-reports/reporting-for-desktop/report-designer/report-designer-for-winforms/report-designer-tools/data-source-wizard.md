---
title: Data Source Wizard
---
# Data Source Wizard

The Data Source Wizard allows you to configure a data source and retrieve its data. 

The first page allows you to create or select an existing data connection.

![Select existing data connection](../../../images/win-data-source-wizard-existing-connection.png)

If you chose a new connection, the next page allows you to select the data connection type.

![Select data connection type](../../../images/eurd-ReportWizard-SelectDataSourceType.png)

You can select a provider and click the “star” icon to pin frequently used database providers as favorites. Favorite providers appear at the top of the list for quick access:

![Pin favorite database providers](../../../images/eud-data-source-wizard-favorites.png)

Use the search panel to filter the connection type list:

![Search connection types](../../../images/eud-data-source-wizard-search-panel.png)

## Use the Data Source Wizard

The Data Source Wizard allows you to do the following:

* [Add a new data-bound report](../add-new-reports.md) to your application using the [Report Wizard](report-wizard.md), which contains the Data Source Wizard pages.
	
	![Create data-bound report](../../../images/eurd-wizard-databaound-report.png)

* Bind an existing report or its [Detail Report band](../introduction-to-banded-reports.md) to data. To invoke this Wizard, click **Add Data Source** on the [Ribbon](ui-panels/toolbar.md)'s **Home** page.

    ![Add Data Source ribbon button](../../../images/eurd-win-add-new-report-data-source-ribbon.png)
	
    Alternatively, click the report's smart tag, expand the **DataSource** property's drop-down menu and click **Add Report Data Source**.

	![Add data source via smart tag](../../../images/eurd-win-add-report-data-source.png)
	
* Connect the [Chart](../use-report-elements/use-charts-and-pivot-grids.md), [Cross Tab](../use-report-elements/use-cross-tabs.md) and [Sparkline](../use-report-elements/use-gauges-and-sparklines.md) report controls to individual data sources.

    You can invoke the Data Source Wizard using the **Add Data Source** command on the **Chart** | **Design** contextual page.

    ![Chart Add Data Source button](../../../images/eurd-win-add-chart-data-source-ribbon.png)

    You can invoke the Data Source Wizard using the **DataSource** property in the chart's smart tag.
	
	![Chart DataSource property menu](../../../images/eurd-win-addchartdatasource.png)

## Supported Data Source Types

The wizard supports the following data source types:

* [Database](data-source-wizard/connect-to-a-database.md)
	
	Obtains data from all major data providers (Microsoft SQL Server, XML data, Microsoft Access, Oracle, etc.).
* [Entity Framework](data-source-wizard/connect-to-an-entity-framework-data-source.md)
	
	Supports binding to a Microsoft ADO.NET Entity Framework data source.
* [Object Binding](data-source-wizard/connect-to-an-object-data-source.md)
	
	Connects to a data object.
* [Excel File](data-source-wizard/connect-to-an-excel-data-source.md)
	
	Obtains data from Microsoft Excel workbooks (XLS, XLSX or XLSM files) or CSV files.
* [JSON](data-source-wizard/connect-to-a-json-data-source.md)

	Connects to JSON-formatted data.

* [MongoDB](data-source-wizard/connect-to-a-mongo-db.md)

	Connects to a MongoDB instance.

* [XPO](data-source-wizard/connect-to-an-xpo-data-source.md)

	Allows you to bind to **XPO** data.

* [No Data](data-source-wizard/no-data.md)

	Allows you design a report that is not bound to a data source.	
