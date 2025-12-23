---
title: Data Source Wizard
---
# Data Source Wizard

The Data Source Wizard enables you to configure a data source and retrieve the required data. It supports the following data source types:

* [Database param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Obtains data from all major data providers (Microsoft SQL Server, XML data, Microsoft Access, Oracle, etc.).
* [Entity Framework param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Supports binding to a Microsoft ADO.NET Entity Framework data source.
* [Object Binding param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Connects to a data object.
* [Excel File param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Obtains data from Microsoft Excel workbooks (XLS, XLSX or XLSM files) or CSV files.
* [JSON param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

	Connects to JSON-formatted data.

* [XPO param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

	Allows you to bind to **XPO** data.

* [No Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

	Allows you design a report that is not bound to a data source.	

![ReportWizard-SelectDataSourceType](..\/..\/..\/images/eurd-ReportWizard-SelectDataSourceType.png)

The Data Source Wizard allows you to do the following:

* [Add a new data-bound report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to your application using the [Report Wizard param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , which contains the Data Source Wizard pages.
	
	![report-wizard-databaound-report-01](..\/..\/..\/images/eurd-wizard-databaound-report.png)

* Bind an existing report or its [Detail Report band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to data. To invoke this Wizard, click **Add Data Source** on the [Ribbon param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 's **Home** page.

    ![eurd-win-add-report-data-source](..\/..\/..\/images/eurd-win-add-new-report-data-source-ribbon.png)
	
    Alternatively, click the report's smart tag, expand the **DataSource** property's drop-down menu and click **Add Report Data Source**.

	![eurd-win-add-report-data-source](..\/..\/..\/images/eurd-win-add-report-data-source.png)
	
* Connect the [Chart param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , [Cross Tab param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [Sparkline param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  report controls to individual data sources.

    You can invoke the Data Source Wizard using the **Add Data Source** command on the **Chart** | **Design** contextual page.

    ![eurd-win-add-chart-data-source-ribbon](..\/..\/..\/images/eurd-win-add-chart-data-source-ribbon.png)

    You can invoke the Data Source Wizard using the **DataSource** property in the chart's smart tag.
	
	![HowTo - AddChartDataSource](..\/..\/..\/images/eurd-win-addchartdatasource.png)