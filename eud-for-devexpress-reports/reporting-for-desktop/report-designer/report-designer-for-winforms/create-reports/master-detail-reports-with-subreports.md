---
title: Master-Detail Reports with Subreports
author: Anna Gubareva
---
# Master-Detail Reports with Subreports

This tutorial demonstrates how to create a master-detail report using the [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control. This approach is useful if your data source does not contain master-detail relationship or you prefer to store master and detail reports in different files. Another approach is described at [Create a Master-Detail Report (Use Detail Report Bands) param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

## <a name="master"></a>Create a Master Report

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or [open an existing one param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to use it as a master report.

2. [Bind the report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to a required data table.

3. Drop the required data fields from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the [Detail param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band.

    ![](..\/..\/..\/images/eurd-win-master-report-layout.png)

## <a name="detail"></a>Create the Detail Report

1. [Add one more blank report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to use it as a detail report.

2. [Bind it to data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . For instance, use another table of the same database as for the master report. 

3. Switch to the **Field List**, select the data fields while holding down CTRL or SHIFT and drag-and-drop them onto the Detail band.
	
	![](..\/..\/..\/images/eurd-win-detail-report-layout.png)

4. Add parameter to the detail report. Right-click the **Parameters** section in the **Field List** and choose **Add Parameter** in the context menu.
	
	![](..\/..\/..\/images/eurd-win-detail-report-add-parameter.png)

5. In the invoked **Add New Parameter** dialog, specify the parameter's **Name** and **Type** as well as disable the **Show in the parameters panel** option.
	
	![](..\/..\/..\/images/eurd-win-detail-report-parameter-settings.png)

6. Click the report's smart tag, and in its actions list, click the **Filter String** property's ellipsis button.
	
	In the invoked **FilterString Editor**, construct an expression where the required data field is compared to the created parameter. To access the parameter, click the icon on the right until it turns into a question mark.
	
	![](..\/..\/..\/images/eurd-win-detail-report-filter-string.png)

7. [Save the detail report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  by selecting **Save** | **Save As** in the toolbar. In the invoked standard **Save** dialog, specify the folder and file name.

	![](..\/..\/..\/images/eurd-win-detail-report-save-dialog.png)

## <a name="subreport"></a>Embed the Subreport
1. Switch back to the master report and drop the [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the **Detail** band.
	
	![](..\/..\/..\/images/eurd-win-master-report-add-subreport.png)

2. Click the subreport's smart tag and clcik the **Report Source URL** property's ellipsis button. In the invoked **Open** dialog, select the previously saved detail report.
	
	![](..\/..\/..\/images/eurd-win-master-report-subreport-report-source-url.png)
	
3. Bind the subreport's parameter used as a filter criterion to the master report's corresponding data field, which serve as a source of the parameter value. To do this, click the subreport's smart tag and select **Edit Parameter Bindings** in the invoked actions list.
	
	![](..\/..\/..\/images/eurd-win-master-report-subreport-edit-parameter-bindings.png)
	
4. In the invoked **Parameter Binding Collection Editor**, click **Add** to add new binding. In the property list, specify the data field to which you want to bind a subreport parameter and the name of the parameter that you want to bind.
	
	![](..\/..\/..\/images/eurd-win-master-report-subreport-parameter-binding-editor.png)

5. If required, customize the report's [appearance param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [format values param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

## <a name="result"></a>View the Result

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the resulting report.

![](..\/..\/..\/images/eurd-win-master-detail-result.png)