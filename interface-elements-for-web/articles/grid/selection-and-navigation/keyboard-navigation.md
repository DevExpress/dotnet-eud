---
title: Keyboard Navigation
author: Andrey Trukhatchev
legacyId: 8451
---
# Keyboard Navigation
If keyboard support is enabled within the GridView, its primary navigation operations (such as accessing the grid within the form, moving focus through grid rows, row selection, row expanding/collapsing, paging) can be quickly and effectively performed, using a keyboard as an alternative to a pointing device.

The enabled keyboard navigation activates the following grid features:
* **Access Key** - The grid control can be easily accessed (focused) by using a keyboard shortcut. This shortcut combines the preset CTRL+SHIFT combination with a single character string specified by an application developer. For example, setting the access key of a grid control to the string "G" indicates that an end-user can navigate to the grid by pressing CTRL+SHIFT+G.
* **Focused Row** - Focus can be moved between rows by using the UP and DOWN ARROW keys. The LEFT and RIGHT ARROW keys can also be used to move row focus, but these keys initially try to collapse/expand a row and, if it's impossible, only then do they move focus. Moving focus from the ultimate (first or last) row within a page changes the page within the grid, if possible.
* **Row Selection** - The SPACE key can be used to mark a focused row as selected/unselected. This works if selection can be applied to a row - that is, if it's not a group or detail row, the multiple row selection mode is enabled, or the row contains a selection check box or button. Multiple rows can be easily selected, by moving row focus using the ARROW keys (UP/DOWN or LEFT/RIGHT) while holding down the SHIFT key.
* **Expanding/Collapsing Rows** - The PLUS and MINUS keys can be used respectively, to expand and collapse group and detail rows. In addition, row collapsing and expanding can be performed using the LEFT and RIGHT ARROW keys.
* **Paging** - The SHIFT+PAGE UP and SHIFT+PAGE DOWN key combinations can be used to go to the next/previous grid page.