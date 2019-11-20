---
title: 'Create a Report with Cross-Band Content and Populated Empty Space'
author: Sergey Andreev
---
# Create a Report with Cross-Band Content and Populated Empty Space

This tutorial describes how to create an invoice report with the following layout options:

- Print part of the content across bands (the blue panel);
- Populate the empty space between the detail and footer information with blank rows.

![](../../../../images/eurd-win-underlay-report-preview-6.png)

This topic assumes that you have a report that groups data source data into invoices and prints each invoice on a separate page.

![](../../../../images/eurd-win-underlay-report-preview-0.png)

## Add Line Numbers

1. Right-click the [Detail band](../introduction-to-banded-reports.md)'s first cell and select Insert / Column to Left from the context menu.

	![](../../../../images/eurd-win-underlay-report-add-cell.png)

1. Select the new cell and specify the following property values:

	* **Summary**: _Report_
	* **Expression**: _sumRecordNumber()_

	![](../../../../images/eurd-win-underlay-report-add-line-numbers.png)

	Each row now includes a row number.

![](../../../../images/eurd-win-underlay-report-preview-3.png)

## Populate the Empty Space

Add empty lines to invoices to populate the empty space between the _Detail_ band's data and the totals.

Click the _Detail_ band's smart tag and check the **Fill Empty Space** property.

![](../../../../images/eurd-win-underlay-report-fillemptyspace.png)

Each invoice now includes the numbered lines that continue until the totals.

![](../../../../images/eurd-win-underlay-report-preview-4.png)

## Add Cross-Band Data

Add a panel with recipient details across the entire group. Place the panel on a separate _GroupHeader_ band that is printed on the background of other bands.

1. Add another _GroupHeader_ band to the top of the report. Click the added band's smart tag and set the **Print Across Bands** property. This makes the band content start at the top of the _GroupHeader1_ and end at the bottom of the _GroupFooter1_ band.

	![](../../../../images/eurd-win-underlay-report-printundernextband.png)

	> [!Tip]
	> Choose a _PageHeader_ band instead of the _GroupHeader_ to limit the cross-band content to a page, even if the _GroupFooter_ is on the next page.

2. As the new _GroupHeader_ band is above the header, it is not grouped. To include it in the grouping, remove the group field from the _GroupHeader1_ band, and [add it to GroupHeader2](#group-data).

1. Add a [Panel](../use-report-elements/use-basic-report-controls/panel.md) control to the _GroupHeader_. Specify the panel's **Background Color** and drop fields onto the panel.

	![](../../../../images/eurd-win-underlay-report-add-recipient.png)

4. Adjust the panel's width and height. The height should match the page height, as the _GroupFooter_ is printed at the bottom of the page.

	![](../../../../images/eurd-win-underlay-report-adjust-crossband-height.png)

1. Switch to Print Preview. The panel is printed on the background of the group content.

	![](../../../../images/eurd-win-underlay-report-preview-5.png)

1. Adjust the content in other bands to print it side-by-side with the panel.

	![](../../../../images/eurd-win-underlay-report-adjust-width.png)

See the final report in Print Preview.

![](../../../../images/eurd-win-underlay-report-preview-6.png)