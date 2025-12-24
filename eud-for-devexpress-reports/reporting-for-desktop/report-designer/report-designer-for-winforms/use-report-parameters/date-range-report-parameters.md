---
title: Date Range Report Parameters
author: Sergey Andreev
---

# Range Report Parameters

This topic describes how to create **date range** and **time range** parameters and filter a report’s data by the specified date or time values.


## Create a Range Parameter in the Report Designer

Follow the steps below to add a range parameter to a report in the [Report Designer](../../report-designer-for-winforms.md):

1. [Create a report parameter](create-a-report-parameter.md).
2. In the *Add New Parameter* dialog, specify parameter options:
   
    - **Parameter type**: *Date and Time*, *Date*, or *Time*
    - **Value Source**: *Range Parameters*
   
    The **Start Parameter** and **End Parameter** sections that appear allow you to configure options to create a date or time range:

    ![The "Add new parameter" dialog for a range parameter](../../../images/use-date-ranges-design-add-param-dialog.png)

3. You can change the *Name* and initial static *Value* for the **Start Parameter** and **End Parameter**. To specify an [expression](../use-expressions.md) instead of a static value, the **Value** option's ellipsis button and use the **Expression Editor** dialog:

    ![The "Add new parameter" dialog for a range parameter - Expression](../../../images/use-date-ranges-design-value-expression.png)

4. [Reference the created range parameter](reference-report-parameters.md). You can reference this parameter in the report’s filter string, in expressions, and in a control's **Text** property. You can also bind control and data source parameters to report parameters.

    We recommend that you use the following functions with range parameters in expressions and filter strings:

    - `InDateRange(Date, FromDate, ToDate)` - equivalent to the `FromDate <= Date && Value < Date` expression.
    - `InTimeRange(Time, FromTime, ToTime)` - equivalent to the `FromTime <= Time && Time < ToTime` expression (including cases where the range spans midnight, such as 23:00-01:00).
    - `OutOfTimeRange(Time, FromTime, ToTime)` - equivalent to the `FromTime > Time || Time => ToTime` expression (including cases where the range spans midnight, such as 23:00-01:00).

    The image below filters the report's data by the following filter string:

    `InDateRange([ShippedDate], ?paramDateRange_Start, ?paramDateRange_End) `

    ![Reference the created range parameter in the filter string](../../../images/use-date-ranges-filterstring.png)


When you switch to the report's **Print Preview** tab, the [Parameters panel](parameters-panel.md) displays the newly created range parameter. Click the editor to set a range. The editor type depends on the parameter type.

After you submit start and end values, the report document shows filtered data.
