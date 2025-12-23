---
title: Expressions Panel
author: Anna Vekhina
---
# Expressions Panel

The **Expressions Panel** allows you to assign expressions to various element properties. The expressions are evaluated at runtime before a document is generated. The Report Designer displays this panel if **expression bindings** are enabled.

Click the ellipsis button next to a property editor to invoke the [Expression Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , that allows you to specify custom expressions.

![](..\/..\/..\/images/eurd-web-expressions-panel.png)

