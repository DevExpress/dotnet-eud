---
title: 'Use Data-Driven Page Sequence'
owner: Sergey Andreev
---

# Use Data-Driven Page Sequence

This topic describes how to combine a table report that uses Portrait page orientation and a chart report that uses Landscape page orientation.

![eurd-merge-reports](../../../images/eurd-merge-reports.png)

Follow the steps below to create a combined report:

## Create a Chart Report

1. Create a report that shows data in the chart form. [Bind](../bind-to-data/bind-a-report-to-a-database.md) the report to a data source. Set the report's **Landscape** property to **true** to enable the Landscape page orientation.

    ![eurd-merge-chart-report](../../../images/eurd-merge-chart-report.png)

1. Add a parameter to your chart report to identify which data to use for the chart. Switch to the **Field List** tab and click the plus sign next to **Parameters**.

    ![eurd-fieldlist-addparameter](../../../images/eurd-fieldlist-addparameter.png)

1. Click the created parameter's edit icon and set its **Name** and **Type**, and uncheck the **Visible** option.

    ![eurd-report-param](../../../images/eurd-report-param.png)

1. Switch to the report's **Properties** tab. Click the **Filter String** option's ellipsis button.

    ![eurd-report-filterstring](../../../images/eurd-report-filterstring.png)

1. In the [Filter Editor](../shape-report-data/filter-data/filter-data-at-the-report-level.md) dialog, construct an expression to compare the key data field to the created parameter.

    ![eurd-report-param-2](../../../images/eurd-report-param-2.png)

1. Save the report.

## Create the Base Report

1. Create a report [bound](../bind-to-data/bind-a-report-to-data.md) to the same data source as the chart report, and arrange a layout like the one shown below:

    ![xtrareports-create-report](../../../images/eurd-merge-products-report-layout.png)

1. Switch to the **Actions** tab and click **Insert Group Footer**.

	![eurd-merge-add-group-footer](../../../images/eurd-merge-add-group-footer.png)

1. Drag a [Subreport](../use-report-elements/use-basic-report-controls/subreport.md) item from the Toolbox onto the added group footer band.

    ![xtrareports-add-subreport](../../../images/eurd-merge-add-subreport.png)

1. Click the subreport control's smart tag. In the **Sub-Report Tasks** window, set the **Report Source** parameter to the chart report's location.

    ![xtrareports-add-subreport](../../../images/eurd-merge-configure-subreport.png)

1. Enable the **Generate Own Pages** option to print the embedded report on separate pages and use its own page settings.

    ![xtrareports-subreport-enable-generateownpages](../../../images/eurd-merge-enable-generateownpages-2.png)

1. Bind the chart report's parameter to the base report's data field. Switch to the subreport's **Field List** tab and click the plus icon next to **Parameters**.

    ![xtrareports-add-subreport](../../../images/eurd-merge-subreport-add-parameter.png)

1. Click the edit icon next to the added parameter and specify the parameter's **Name** and **Type**. Uncheck the **Visible** property.

    ![xtrareports-add-subreport](../../../images/eurd-merge-subreport-edit-parameter.png)

1. Switch to Preview mode to see the combined report.

    ![xtrareports-merge-reports](../../../images/eurd-merge-reports.png)

Your base report's **Table of Contents** and **Document Map** include bookmarks from the embedded report. Use the **Parent Bookmark** property to specify the nesting level for the embedded report's bookmarks.
