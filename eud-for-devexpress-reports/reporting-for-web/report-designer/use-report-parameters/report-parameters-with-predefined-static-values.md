---
title: Report Parameters with Predefined Static Values
author: Sergey Andreev
---

# Report Parameters with Predefined Static Values

You can create a list of predefined values for a report parameter.

![Create a report parameter with predefined static values](..\/..\/images/eurd-web-static-parameter-values.png)

When you open a report's **Print Preview**, you can select a value from this list in the [Parameters panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![Create a report parameter with predefined static values - Preview](..\/..\/images/report-parameter-with-predefined-static-values-preview.png)

## Create a List of Predefined Values in the Report Designer

Follow the steps below to create a parameter with a list of predefined static values in the [Report Designer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } :

1. Create a report parameter as described in this topic: [Create a Report Parameter param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
2. Set the parameter's **Value Source** option to **Static List**. A grid appears in the **Add New Parameter** dialog and allows you to specify a list of static parameter values. 

    ![Specify static values for a report parameter](..\/..\/images/parameter-specify-static-values.png)

    Each value should have a description. This description is displayed in the [Parameters panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
