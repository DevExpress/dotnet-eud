---
title: Add a Report to the End/Beginning
owner: Sergey Andreev
---

# Add a Report to the End/Beginning

Follow the steps below to add a separate report to the end of another report and print it as a single job.

![xtrareports-merge-endreport-layouts](..\/..\/..\/images/eurd-merge-endreport-layouts.png)

1. Right-click the base report and select the **Insert Band** / **Report Footer** item in the context menu.

	![toolbox-drop-report-control-label](..\/..\/..\/images/eurd-merge-add-report-footer.png)

1. Drag a [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  item from the Toolbox onto the created Report Footer band.

	![toolbox-drop-report-control-label](..\/..\/..\/images/eurd-merge-add-subreport-2.png)

    > [!Tip]
    > To add a report to the beginning of another report (for instance, to add a title page), use the **Report Header** band instead.

1. Click the subreport's smart tag and specify a report in the **Sub-Report Tasks** window:

    * Use the **Report Source** property to assign a predefined report from the Designer.
    * Use the **Report Source Url** property to assign a custom report.

    ![xtrareports-add-subreport](..\/..\/..\/images/eurd-merge-configure-subreport-2.png)

1. Enable the **Generate Own Pages** option to print the embedded report on separate pages and use its own page settings.

    ![xtrareports-subreport-enable-generateownpages](..\/..\/..\/images/eurd-merge-enable-generateownpages-2.png)

1. Switch to Preview mode to see the combined report.

    ![title-report-page-result](..\/..\/..\/images/eurd-merge-endreport-result.png)
