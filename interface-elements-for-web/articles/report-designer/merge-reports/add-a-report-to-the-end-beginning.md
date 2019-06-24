---
title: Add a Report to the End/Beginning
owner: Sergey Andreev
---

# Add a Report to the End/Beginning

Follow the steps below to add a separate report to the end of another report and print it as a single job.

![xtrareports-merge-endreport-layouts](../../../images/eurd-merge-endreport-layouts.png)

1. Click **Insert Report Footer Band** in the **Actions** panel.

	![toolbox-drop-report-control-label](../../../images/eurd-merge-add-report-footer.png)

1. Drag a [Subreport](../use-report-elements/use-basic-report-controls/subreport.md) item from the Toolbox onto the created Report Footer band.

	![toolbox-drop-report-control-label](../../../images/eurd-merge-add-subreport-2.png)

    > [!Tip]
    > To add a report to the beginning of another report (for instance, to add a title page), use the **Report Header** band instead.

1. In the Subreport's **Actions** panel, set the **Report Source Url** parameter to the report that you want to insert.

    ![xtrareports-add-subreport](../../../images/eurd-merge-configure-subreport-2.png)

1. Enable the **Generate Own Pages** option in the Subreport's **Behavior** panel to print the embedded report on separate pages and use its own page settings.

    ![xtrareports-subreport-enable-generateownpages](../../../images/eurd-merge-enable-generateownpages-2.png)

1. Switch to Preview mode to see the combined report.

    ![title-report-page-result](../../../images/eurd-merge-endreport-result.png)
