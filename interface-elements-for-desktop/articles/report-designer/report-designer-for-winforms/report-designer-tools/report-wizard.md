---
title: Report Wizard
owner: Mary Sammal
---
# Report Wizard

The Report Wizard allows you to add a report using one of the following templates:

* [Empty Report](xref:4270)
	
	Creates a new blank report that is not bound to a data source.
* [Data-bound Report](xref:4271)
	
	Allows you to connect the created report to a data source and configure basic report layout settings (optional).
* [Template Report](xref:119389)
	
	Enables you to create a new report based on available predefined templates.
* [Label Report](xref:4242)
	
	Runs the Label Wizard that enables you to select from hundreds of customizable layouts to create labels, badges or price tags.

![eurd-win-report-wizard](../../../../images/eurd-win-report-wizard.png)

## Run the Report Wizard

Use one of the following ways to invoke the Report Wizard.

- Create a new report

    Use the [New Report via Wizard](add-new-reports.md) command to create a new report based on one of the templates the Report Wizard provides.

- Edit an existing report

    Click the report's Smart Tag and then the **Design in Report Wizard...** context link in the invoked actions list.

    > [!Note]
    > The report layout the Report Wizard creates overrides the initial report layout.


## Report Wizard Pages

Choose a report template on the first wizard page (see above). The wizard provides the following page series for each of the available report templates:

* [Empty Report](report-wizard\empty-report.md)
* [Data-bound Report](report-wizard\data-bound-report.md)
    
    * [Select the Data Source Type](report-wizard\data-bound-report\select-the-data-source-type.md)
        
        * Connect to a Database
            
            * [Select a Data Connection](report-wizard\data-bound-report\connect-to-a-database\select-a-data-connection.md)
            * [Specify a Connection String](report-wizard\data-bound-report\connect-to-a-database\specify-a-connection-string.md)
            * [Save the Connection String](report-wizard\data-bound-report\connect-to-a-database\save-the-connection-string.md)
            * [Create a Query or Select a Stored Procedure](report-wizard\data-bound-report\connect-to-a-database\create-a-query-or-select-a-stored-procedure.md)
            * [Configure Query Parameters](report-wizard\data-bound-report\connect-to-a-database\configure-query-parameters.md)
        * Connect to an Entity Framework Data Source
            
            * [Select the Data Context](report-wizard\data-bound-report\connect-to-an-entity-framework-data-source\select-the-data-context.md)
            * [Select a Connection String](report-wizard\data-bound-report\connect-to-an-entity-framework-data-source\select-a-connection-string.md)
            * [Specify a Connection String](report-wizard\data-bound-report\connect-to-an-entity-framework-data-source\specify-a-connection-string.md)
            * [Bind to a Stored Procedure](report-wizard\data-bound-report\connect-to-an-entity-framework-data-source\bind-to-a-stored-procedure.md)
            * [Select a Data Member](report-wizard\data-bound-report\connect-to-an-entity-framework-data-source\select-a-data-member.md)
            * [Configure Filters](report-wizard\data-bound-report\connect-to-an-entity-framework-data-source\configure-filters.md)
        * Connect to an Object Data Source
            
            * [Select an Assembly](report-wizard\data-bound-report\connect-to-an-object-data-source\select-an-assembly.md)
            * [Select a Data Source Type](report-wizard\data-bound-report\connect-to-an-object-data-source\select-a-data-source-type.md)
            * [Select a Data Source Member](report-wizard\data-bound-report\connect-to-an-object-data-source\select-a-data-source-member.md)
            * [Specify the Member Parameters](report-wizard\data-bound-report\connect-to-an-object-data-source\specify-the-member-parameters.md)
            * [Select the Data Binding Mode](report-wizard\data-bound-report\connect-to-an-object-data-source\select-the-data-binding-mode.md)
            * [Select a Data Source Constructor](report-wizard\data-bound-report\connect-to-an-object-data-source\select-a-data-source-constructor.md)
            * [Specify the Constructor Parameters](report-wizard\data-bound-report\connect-to-an-object-data-source\specify-the-constructor-parameters.md)
        * Connect to an Excel Data Source
            
            * [Select an Excel Workbook or CSV File](report-wizard\data-bound-report\connect-to-an-excel-data-source\select-an-excel-workbook-or-csv-file.md)
            * [Specify Import Settings](report-wizard\data-bound-report\connect-to-an-excel-data-source\specify-import-settings.md)
            * [Select a Worksheet, Table or Named Range](report-wizard\data-bound-report\connect-to-an-excel-data-source\select-a-worksheet-table-or-named-range.md)
            * [Choose Columns](report-wizard\data-bound-report\connect-to-an-excel-data-source\choose-columns.md)
        * [Choose Fields to Display in a Report (Multi-Query Version)](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\data-bound-report\choose-fields-to-display-in-a-report.md)
        * [Add Grouping Levels (Multi-Query Version)](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\data-bound-report\add-grouping-levels.md)
        * [Specify Summary Options (Multi-Query Version)](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\data-bound-report\specify-summary-options.md)
        * [Set the Report Title](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\data-bound-report\set-the-report-title.md)
* [Template Report](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\template-report.md)
    
    * [Choose a Report Template](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\template-report\choose-a-report-template.md)
    * [Map Report Template Fields](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\template-report\map-report-template-fields.md)
    * [Specify Report Template Options](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\template-report\specify-report-template-options.md)
* [Label Report](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\label-report.md)
    
    * [Select the Label Type](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\label-report\select-the-label-type.md)
    * [Customize the Label Options](report-designer\report-designer-for-winforms\report-designer-tools\report-wizard\label-report\customize-the-label-options.md)