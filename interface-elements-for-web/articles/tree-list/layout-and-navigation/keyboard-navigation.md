---
title: Keyboard Navigation
author: Andrey Trukhatchev
legacyId: 8452
---
# Keyboard Navigation
If keyboard support is enabled within the TreeList, its primary navigation operations (such as accessing the control within the form, moving focus through its nodes, node selection and expanding/collapsing, paging) can be quickly and effectively performed, using a keyboard as an alternative to a pointing device.

The enabled keyboard navigation activates the following features:
* **Access Key** - The TreeList control can be easily accessed (focused) by using a keyboard shortcut. This shortcut combines the preset CTRL+SHIFT combination with a single character string specified by an application developer. For example, setting the access key of a TreeList control to the string "T" indicates that an end-user can navigate to the grid by pressing CTRL+SHIFT+T.
* **Focused Node** - Focus can be moved between nodes by using the UP and DOWN ARROW keys. The LEFT and RIGHT ARROW keys can also be used to move node focus, but these keys initially try to collapse/expand a node and, if it's impossible, only then do they move focus. Moving focus from the ultimate (first or last) node within a page changes the page within the TreeList, if applicable.
* **Node Selection** - The SPACE key can be used to mark a focused node as selected/unselected. This works if selection can be applied to a node. If the recursive selection is disabled, multiple nodes can be easily selected, by moving row focus using the ARROW keys (UP/DOWN or LEFT/RIGHT) while holding down the SHIFT key.
* **Expanding/Collapsing Nodes** - The PLUS and MINUS keys can be used to expand and collapse nodes, respectively. In addition, node collapsing and expanding can be performed using the LEFT and RIGHT ARROW keys.
* **Paging** - The SHIFT+PAGE UP and SHIFT+PAGE DOWN key combinations can be used to go to the next/previous TreeList page.