---
title: Sort Data by a Custom Field
author: Anna Gubareva
---
# Sort Data by a Custom Field

This tutorial illustrates how to sort a report against a custom criteria, in particular, sort data by the number of characters in the data field value. 

1. Create a new or open an existing data-bound report.
	
	You cannot apply grouping unless your report is bound to a data source.

2. Create a [calculated field param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , right-click any item inside the data source and select **Add Calculated Field**.
	
	![](..\/..\/..\/..\/images/eurd-win-sort-data-create-calculated-field.png)	

3. Select the calculated field, and in the [Property Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , click the **Expression** property's ellipsis button.
	
	![](..\/..\/..\/..\/images/eurd-win-sort-data-calculated-field-settings.png)
	

4. In the invoked **Expression Editor**, select the required date-time function and define the data field's name in **[**square brackets**]**. For example,  use the **Len([ProductName])** function to return the number of characters extracted from the **ProductName** data field.
	
	![](..\/..\/..\/..\/images/eurd-win-sort-data-calculated-field-expression.png)
	
	Click **OK** to close the editor and save the changes.
5. In the [Group and Sort param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel, click **Add a Sort** and select the calculated field from the invoked drop-down menu.
	
	![](..\/..\/..\/..\/images/eurd-win-sort-data-by-calculated-field.png)
	
	The **Sort Order** drop-down list allows you to define the sort order within the group (ascending or descending).

6. Drag the corresponding field from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the report area and switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the result.

    ![](..\/..\/..\/..\/images/eurd-win-sort-data-by-calculated-field-result.png)