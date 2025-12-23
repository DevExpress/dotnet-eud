---
title: Add Controls to a Report
author: Anna Vekhina
---
# Add Controls to a Report

## Add Report Controls
To display a data field's value in your report, drag the corresponding item from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and drop it onto the report's detail band. This creates a new report control bound to the corresponding field.

![](..\/..\/..\/images/eurd-web-drop-field-from-field-list.png)

You can also use the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to add other controls to your report and display content such as text, images, charts, barcodes, and so on.

![](..\/..\/..\/images/eurd-web-report-add-label.png)

This document describes how to add the most commonly used controls to a report. See [Use Report Elements param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  for a complete list of available controls.

## Display Text
Use the following controls to display text in a report:

* [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Displays plain text in a report. 

	![](..\/..\/..\/images/eurd-web-label.png)
	

* [Rich Text param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Displays rich text in a report. You can apply different font settings to the control's content and load content from an external HTML file.

	![](..\/..\/..\/images/eurd-web-rich-text.png)
	

* [Table param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Contains any number of cells arranged in one or more rows.
	Each table cell can display plain text or contain other controls.

	![](..\/..\/..\/images/eurd-web-table.png)
	
* [Character Comb param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
	
	Displays each character in a separate cell and can be used to create printed forms.

	![](..\/..\/..\/images/eurd-web-character-comb.png)
	

Double-click any of these controls to invoke an in-place editor where you can enter text.

![](..\/..\/..\/images/eurd-web-in-place-editor.png)

Press CTRL+Enter to submit changes and close this mode.

You can use corresponding properties of the **Appearance** category to access the selected control's font and alignment settings.

![](..\/..\/..\/images/eurd-web-label-appearance.png)


Labels and other text-oriented controls can display the following content:

* **Static content**
	
	A control's content does not change once it is specified in a published document.

	![](..\/..\/..\/images/eurd-web-static-content.png)

* **Dynamic content**
	
	A connected data source supplies this content. In a published document, it changes according to the printed data source record.

	![](..\/..\/..\/images/eurd-web-dynamic-content.png)
	
	You can use the [Format String Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to format dynamic content.

	![](..\/..\/..\/images/eurd-web-format-string-editor.png)
	

* **Mixed content**
	
	You can combine labels' and other text-oriented controls' static and dynamic content within the same control.	
	
	Use the **Format String** property in the **Action** category to format this field's value.

	![](..\/..\/..\/images/eurd-web-format-string-property.png)

## Display Page Information
Use the [Page Info param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control to display information about document pages, such as the current page number and/or total number of pages.

![](..\/..\/..\/images/eurd-web-page-info.png)

You can also use this control to add information about a report's author and the document's creation date.

See the following tutorials for detailed instructions:

* [Add Page Numbers param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Display the User Name in a Report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Display the Current Date and Time in a Report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

## Display Check Boxes, Images and Barcodes
Drop a Boolean data field from the Field List onto a report to create a [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control bound to that field.

![](..\/..\/..\/images/eurd-web-check-box.png)

Check boxes can display different states depending on the underlying data values.

![](..\/..\/..\/images/eurd-web-check-boxe-states.png)

Use the [Picture Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control to display images in a report. You can load an image from an external file, from a bound data source, or from a web location using the specified URL.

![](..\/..\/..\/images/eurd-web-picture-box.png)

To display barcodes, use the [Barcode param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control.

![](..\/..\/..\/images/eurd-web-bar-code.png)

## <a name="drawinglinesshapes"></a>Drawing Lines and Shapes
Use the [Shape param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control to draw simple graphics in a report (circles, crosses or arrows).

![](..\/..\/..\/images/eurd-web-display-shapes.png)

The [Line param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control enables you to draw straight or slanted lines in a single band.

![](..\/..\/..\/images/eurd-web-lines.png)

The [Cross-Band Line and Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  controls enable you to draw lines and boxes spanning multiple report bands.
