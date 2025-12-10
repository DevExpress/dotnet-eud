---
title: Calculate Carried Forward/Brought Forward
author: Margarita Zakhodyaeva
---
# Calculate Carried Forward/Brought Forward

## Overview

Carried Forward/Brought Forward summaries refer to the practice of automatically transferring specific values or calculations from one reporting period or data group to another (eliminating the need for manual data entry or redundant calculations).

As the following image illustrates, calculated running summaries are transferred from the report’s page footer to the header of the next page. Values are calculated for the group and are specified by the user. It can involve grouping by monthly expenses, or grouping by month with the cumulative balance of total expenses.

![CarryOver Scheme](~/eud-for-devexpress-reports/reporting-for-desktop/images/carryover-scheme.png)

In Reporting controls, Carried Forward/Brought Forward summaries are represented by the `sumCarryoverSum(Expression)`. function. 

## Example: How to Display Transactions for a User Account

The example shows how to display transactions for a user account. These transactions represent expenses for one month. Records span multiple pages and the summary displayed in the footer of the first page is repeated in the header of the subsequent page.

1. Place the `Label` controls in group header/group footer bands. Enable group header/group footer bands’ **Repeat Every Page** option.

    ![](~/eud-for-devexpress-reports/reporting-for-desktop/images/xrlabel-in-repetitive-bands.png)

2. Bind the `XRLabel` controls to the following expression:

    `sumCarryoverSum([Amount])`

    This allows DevExpress Reports to display the balance on each page.

    ![](~/eud-for-devexpress-reports/reporting-for-desktop/images/display-transactions-for-a-user-account.png)