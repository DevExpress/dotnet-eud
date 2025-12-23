---
title: Table of Contents
author: Anna Vekhina
---
# Table of Contents

## Overview
Once [bookmarks param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  have been assigned to specific report elements, you can generate a table of contents that displays page numbers containing the elements included into the document map.

To implement a table of contents, drop the **Table Of Contents** control from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the report's area. If the report does not contain a [Report Header param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  at the moment, it is created automatically so that the table of contents can be added to it.

![](..\/..\/..\/images/eurd-web-add-table-of-contents-to-report.png)

The following image illustrates the difference in displaying information by a table of contents within a report and in a published document.

![](..\/..\/..\/images/eurd-web-table-of-contents-example.png)


## Table of Contents Structure
The table of contents contains the following elements:

1. A title that displays text and formatting options specified by the **Level Title** property.

2. One or more document levels that provide individual formatting settings to specific nodes of a document map's tree. To access the collection of levels, use the **Levels** property.
	
	Unless levels have been added to a table of contents, a single default level is used to provide common settings to the elements of a document map for which no specific level has yet been assigned.

Refer to the [Add a Table of Contents param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topic for a step-by-step tutorial.
