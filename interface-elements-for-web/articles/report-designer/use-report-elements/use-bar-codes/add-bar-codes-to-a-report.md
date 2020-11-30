---
title: Add Bar Codes to a Report
author: Anna Vekhina
---
# Add Bar Codes to a Report

## Overview

To insert a bar code into a report, drag the **Bar Code** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area.

![](../../../../images/eurd-web-add-bar-code-to-report.png)

After creating the bar code, expand the **Actions** category and select the bar code type (symbology) in the **Symbology** property's drop-down list.
	
![](../../../../images/eurd-web-bar-code-symbology.png)
	
After specifying the symbology, you can customize the type-specific options of the bar code, which are listed under the **Symbology** property.
	
![](../../../../images/eurd-web-bar-code-symbology-property.png)

## Main Options

To specify the bar width (a bar code's resolution), use the following options:
	
* Automatically calculate the bar width according to a bar code's dimensions by enabling the **Auto Module** option;
* Provide a fixed bar width value using the **Module** property.

The following are some additional bar code options:
	
* Use the bar code's **Text** property to provide accompanying text. The **Show Text** property allows you to show or hide this text.

* Use the **Orientation** property to rotate a bar code.

* Use the **Padding** property to specify the indent between bars and the bar code's inner boundaries.

## Bind to Data

You can [bind](../bind-controls-to-data.md) the bar code's **Text** property to a data field obtained from a report's data source. Click the **Text** property's ellipsis button in the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel. The invoked [Expression Editor](../../report-designer-tools/expression-editor.md) allows you to select a data field or construct a complex binding expression with two or more data fields.

![](../../../../images/eurd-web-bar-code-bind-to-data.png)


## Common Errors
The following section explains how to work around the most frequently encountered errors related to the incorrect use of bar codes.

* The following error message is shown in place of the bar code if the control's dimensions are too small to fit the bar code with its specified resolution.
	
	![](../../../../images/eurd-web-bar-code-small-boundaries-error.png)
	
	To get rid of this error, enable the **Auto Module** property and/or increase the bar code's dimensions.

* The following error message appears when the data supplied to a bar code contains characters that are not supported by this bar code type.
	
	![](../../../../images/eurd-web-bar-code-invalid-characters-error.png)
	
	To avoid this error, supply data that applies to a particular bar code specification.
