---
title: Labels and Badges
author: Anna Vekhina
---
# Labels and Badges

This tutorial describes the steps to create a label report that contains employee badges.

![](..\/..\/images/eurd-web-label-report-result.png)

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [bind it param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to a required data source (for instance, to a table that contains information about employees).

2. Open the designer [menu param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and click **New via Wizard**.

    ![](..\/..\/images/eurd-web-report-design-in-report-wizard.png)

3. The wizard guides you through the process of creating a label report. Refer to [Label Report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  for detailed instructions on the wizard's steps. 

    ![](..\/..\/images/eurd-web-fullscreen-report-wizard-label-report.png)

4. After performing the above steps you will see that the report's Detail band is now divided into three differently colored areas. The first area at the left-hand side indicates the actual available band area for controls to be placed within it. The gray area at the right-hand side is intended for the columns in which labels will be displayed, so it cannot be occupied by controls. Finally, the white area specifies an indent between the available and reserved areas.

    ![](..\/..\/images/eurd-web-label-wizard-result.png)

5. Drop the required fields from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the available Detail band's area and adjust the layout.

    ![](..\/..\/images/eurd-web-label-report-layout.png)

    If required, you can apply [mail merge param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to combine several fields within the same [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control.

    For the [Picture Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control, you can set its **Sizing** property to **Zoom Image**.

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the resulting report.

![](..\/..\/images/eurd-web-label-report-result.png)

