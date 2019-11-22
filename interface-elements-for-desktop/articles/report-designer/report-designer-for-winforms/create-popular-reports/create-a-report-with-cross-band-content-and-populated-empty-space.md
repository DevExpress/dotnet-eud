---
title: 'Create a Report with Cross-Band Content and Populated Empty Space'
author: Sergey Andreev
---
# Create a Report with Cross-Band Content and Populated Empty Space

This tutorial describes how to create an invoice report with the following layout options:

- Print part of the content across bands (the blue panel);
- Populate the empty space between the detail and footer information with blank rows.

![](../../../../images/eurd-win-underlay-report-preview-6.png)

## Initial Report

[Create](../add-new-reports.md) or [open](../open-reports.md) a [table report](../create-popular-reports/create-a-table-report.md) that has an empty space between the _Detail_ band and the footer, like the invoice report below.

![](../../../../images/eurd-win-underlay-report-preview-0.png)

## Add Line Numbers

1. Right-click the first cell in the [Detail band](../introduction-to-banded-reports.md)'s table and select **Insert** / **Column to Left** from the context menu.

	![](../../../../images/eurd-win-underlay-report-add-cell.png)

1. Select the new cell and specify the following property values:

	* **Summary**: _Group_
	* **Expression**: _sumRecordNumber()_

	![](../../../../images/eurd-win-underlay-report-add-line-numbers.png)

Each row now includes a number.

![](../../../../images/eurd-win-underlay-report-preview-3.png)

## Populate the Empty Space

Populate the empty space between the _Detail_ band's data and the totals.

Click the _Detail_ band's smart tag and check the **Fill Empty Space** property.

![](../../../../images/eurd-win-underlay-report-fillemptyspace.png)

Invoices now include numbered lines that continue until the totals.

![](../../../../images/eurd-win-underlay-report-preview-4.png)

> [!NOTE]
> Set the **Text** properties of the _Detail_ band's controls to display static text within the added lines.

## Add Cross-Band Data

Follow the steps below to display content across report groups.

1. Right-click the design surface. Select **Insert Band** / **GroupHeader** from the context menu.

	![](../../../../images/eurd-win-underlay-report-add-group-header.png)

	> [!Tip]
	> Choose a _PageHeader_ band instead to display the cross-band content on an entire page.

1. Click the added band's smart tag and set the **Print Across Bands** property.  This displays the band content on the background of the report group.

	![](../../../../images/eurd-win-underlay-report-printundernextband.png)

2. Assign group fields to the added band to include it in each group, and un-assign these fields are specified from the initial _GroupHeader_. Click the new band's smart tag, click the **Group Fields** property's ellipsis button and add group fields in the invoked **Group Field Collection Editor**.

	![](../../../../images/eurd-win-underlay-report-move-group-fields.png)

1. Add a [Panel](../use-report-elements/use-basic-report-controls/panel.md) control to the _GroupHeader_. Specify the panel's **Background Color** and drop fields onto the panel.

	![](../../../../images/eurd-win-underlay-report-add-recipient.png)

4. Adjust the panel's width and height. The height should match the page height, as the footer is printed at the bottom of the page (the _GroupFooter_'s **Print At Bottom** property is enabled).

	![](../../../../images/eurd-win-underlay-report-adjust-crossband-height.png)

1. Switch to Print Preview. The panel is printed on the background of the group content.

	![](../../../../images/eurd-win-underlay-report-preview-5.png)

1. Resize the content in other bands to print it side-by-side with the panel.

	![](../../../../images/eurd-win-underlay-report-adjust-width.png)

See the final report in Print Preview.

![](../../../../images/eurd-win-underlay-report-preview-6.png)