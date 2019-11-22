---
title: 'Create a Report with Cross-Band Content and Populated Empty Space'
author: Sergey Andreev
---
# Create a Report with Cross-Band Content and Populated Empty Space

This tutorial describes how to create an invoice report with the following layout options:

- Print part of the content across bands (the blue panel);
- Populate the empty space between the detail and footer information with blank rows.

![](../../../images/eurd-web-underlay-report-preview-6.png)

This topic assumes that you have a report that groups data source data into invoices and prints each invoice on a separate page.

![](../../../images/eurd-web-underlay-report-preview-0.png)

## Add Line Numbers

1. Select the first cell in the [Detail band](../introduction-to-banded-reports.md)'s table and click **Insert Column to the Left** in the Actions panel.

	![](../../../images/eurd-web-underlay-report-add-cell.png)

1. Select the new cell and set **Summary**/**Running** to _Group_.

	![](../../../images/eurd-web-underlay-report-add-line-numbers.png)

1. Switch to the **Expressions** tab and click the **Text** property's ellipsis button. Specify the _sumRecordNumber()_ expression in the invoked Expression Editor.

	![](../../../images/eurd-web-underlay-report-add-line-numbers-2.png)

	Each row now includes a row number.

![](../../../images/eurd-web-underlay-report-preview-3.png)

## Populate the Empty Space

Add empty lines to invoices to populate the empty space between the _Detail_ band's data and the totals.

Click the _Detail_ band's smart tag and enable the **Fill Empty Space** property.

![](../../../images/eurd-web-underlay-report-fillemptyspace.png)

Each invoice now includes the numbered lines that continue until the totals.

![](../../../images/eurd-web-underlay-report-preview-4.png)

> [!NOTE]
> You can display predefined values instead of empty lines. Specify the predefined values in the **Text** properties of the _Detail_ band's controls.

## Add Cross-Band Data

Add a panel with recipient details across the entire group. Place the panel on a separate _Group Header_ band that is printed on the background of other bands.

1. Select the report and click **Insert Group Header Band** in the Actions group.

	![](../../../images/eurd-web-underlay-report-addgroupheader.png)

1. Click the added band's smart tag and enable the **Print Across Bands** property. This makes the band content start in the background of the group's other bands.

	![](../../../images/eurd-web-underlay-report-printundernextband.png)

	> [!Tip]
	> Choose a _Page Header_ band instead of the _Group Header_ to limit the cross-band content to a page, even if the _Group Footer_ is on the next page.

1. As the new _GroupHeader_ band is above the header, it is not included in the grouping. Move the group fields from the previous _Group Header_ band to the new band.

	![](../../../images/eurd-web-underlay-report-movegroupfields.png)

1. Add a [Panel](../use-report-elements/use-basic-report-controls/panel.md) control to the _GroupHeader_. Specify the panel's **Background Color** and drop fields onto the panel.

	![](../../../images/eurd-web-underlay-report-add-recipient.png)

1. Adjust the panel's width and height. The height should match the page height, as the _GroupFooter_ is printed at the bottom of the page.

	![](../../../images/eurd-web-underlay-report-adjust-crossband-height.png)

1. Switch to Print Preview. The panel is printed on the background of the group content.

	![](../../../images/eurd-web-underlay-report-preview-5.png)

1. Adjust the content in other bands to print it side-by-side with the panel.

	![](../../../images/eurd-web-underlay-report-adjust-width.png)

See the final report in Print Preview.

![](../../../images/eurd-web-underlay-report-preview-6.png)