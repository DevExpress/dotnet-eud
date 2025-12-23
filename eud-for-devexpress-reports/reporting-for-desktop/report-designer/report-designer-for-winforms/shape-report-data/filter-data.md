---
title: Filter Data
author: Anna Gubareva
---
# Filter Data

The topics in this section describe different approaches to filtering data in your reports:

* [Filter Data at the Report Level param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
    
    Use the report's settings demonstrated in this tutorial if you want to load the entire dataset and filter it on the client.

* [Filter Data at the Data Source Level param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

    Filter records at data source level using your data connection query if you are binding to a large data source and want to speed up the retrieval process.

* [Limit the Number of Records to Display param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

    Options described in this topic allow you to emulate the Top N feature in a sorted report or increase the Print Preview performance by rendering only a subset of a report’s data.