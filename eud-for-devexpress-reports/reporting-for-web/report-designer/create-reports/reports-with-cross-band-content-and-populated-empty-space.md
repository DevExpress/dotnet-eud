---
title: 'Reports with Cross-Band Content and Populated Empty Space'
author: Sergey Andreev
---
# Reports with Cross-Band Content and Populated Empty Space

This document describes how to create a report with the following layout options:

- Print part of the content across bands (the blue panel);
- Populate the empty space between the detail and footer information with blank rows.

![](../../../images/eurd-web-underlay-report-preview-6.png)

## Initial Report

In this tutorial, the report [groups data](../shape-report-data/group-and-sort-data.md) by a data source field (the report's group field).

![](../../../images/eurd-web-underlay-report-preview.png)

The _GroupFooter_ band is displayed at the bottom of the page (the **Print At Bottom** property is enabled). There is an empty space between the **Detail** band's data and the footer.

![](../../../images/eurd-web-underlay-report-preview-0.png)

## Add Line Numbers

1. Select the first cell in the [Detail band](../introduction-to-banded-reports.md)'s table and click **Insert Column to the Left** from the cell's context menu.

	![](../../../images/eurd-web-underlay-report-add-cell.png)

2. Select the new cell and set **Summary**/**Running** to _Group_.

	![](../../../images/eurd-web-underlay-report-add-line-numbers.png)

3. Switch to the **Expressions** tab and click the **Text** property's ellipsis button. Specify the _sumRecordNumber()_ expression in the invoked Expression Editor.

	![](../../../images/eurd-web-underlay-report-add-line-numbers-2.png)

	Each row now includes a number.

![](../../../images/eurd-web-underlay-report-preview-3.png)

## Populate the Empty Space

Populate the empty space between the _Detail_ band's data and the footer.

Select the _Detail_ band and enable the **Fill Empty Space** property.

![](../../../images/eurd-web-underlay-report-fillemptyspace.png)

The empty space is now populated with numbered lines.

![](../../../images/eurd-web-underlay-report-preview-4.png)

> [!NOTE]
> Set the **Text** properties of the _Detail_ band's controls to display static text within the added lines.

## Add Cross-Band Data

Add a panel with recipient details across the entire group. Place the panel on a separate _Group Header_ band that is printed on the background of other bands.

1. Select the report and select **Insert Group Header** from the report's context menu

	![](../../../images/eurd-web-underlay-report-addgroupheader.png)

	> [!Tip]
	> Choose a _Page Header_ band instead of the _Group Header_ to display the cross-band content on an entire page.

2. Select the added band and enable the **Print Across Bands** property. This displays the band content on the background of the _GroupHeader1_, _Detail_, and _GroupFooter1_ bands.

	![](../../../images/eurd-web-underlay-report-printundernextband.png)

3. The report's group field is in the _GroupHeader1_ band's **Group Fields** collection. The new band is above **GroupHeader1** and does not participate in the report's group. Move the group field to the new band.

	* Select _GroupHeader1_ and remove the group field from **Group Fields**.

	![](../../../images/eurd-web-underlay-report-removegroupfields.png)

	* Select the new band and add the group field to **Group Fields**.

	![](../../../images/eurd-web-underlay-report-movegroupfields.png)

4. Add a [Panel](../use-report-elements/use-basic-report-controls/panel.md) control to the _Group Header_. Specify the panel's **Background Color** and drop fields onto the panel.

	![](../../../images/eurd-web-underlay-report-add-recipient.png)

5. Adjust the panel's width and height. The height should match the page height, as the footer is printed at the bottom of the page (the _Group Footer_'s **Print At Bottom** property is enabled).

	![](../../../images/eurd-web-underlay-report-adjust-crossband-height.png)

6. Switch to Print Preview. The panel is printed on the background of the group content.

	![](../../../images/eurd-web-underlay-report-preview-5.png)

1. Resize the content in other bands to print it side-by-side with the panel.

	![](../../../images/eurd-web-underlay-report-adjust-width.png)

See the final report in Print Preview.

![](../../../images/eurd-web-underlay-report-preview-6.png)