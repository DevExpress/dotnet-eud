---
title: Predefined Periods
author: Natalia Kazakova
legacyId: 117558
---
# Predefined Periods
The Range Filter dashboard item allows you to add a number of predefined date-time periods that can be used to perform a selection (for instance, _year-to-date_ or _quarter-to-date_).

- [Add Predefined Ranges](#add-predefined-ranges)
- [Select Predefined Ranges](#select-predefined-ranges)

## Add Predefined Ranges
To add predefined ranges, open the Range Filter's [Options](../../ui-elements/dashboard-item-menu.md) menu and go to the **Custom Periods** section. Click "+" to add a new period.

![wdd-range-filter-custom-intervals](../../../../images/img125362.png)

You can specify the following settings for the start/end boundaries.
* **Caption** - Specifies a predefined period caption.
* **Start Mode** - Specifies a mode of the start boundary.
* **End Mode** - Specifies a mode of the end boundary.

The following modes used to set predefined ranges are available.
* **None** - The selection will begin from the start/end of the visible range.
* **Fixed** - Allows you to select a specific date value using the calendar. Use the **Start/End Date** option to set a value.
* **Flow** - Allows you to select a relative date value. The **Interval** option specifies the interval between the current date and the required date. The **Offset** option allows you to set the number of such intervals.
	
	> [!NOTE]
	> Note that the **Offset** option can accept **negative** and **positive** values. Negative values correspond to dates before the current date, while positive values correspond to future dates.

Below you can find some examples of how to set up custom periods:

**Fixed custom periods**

**2018**
- _Start Point_
	- Mode: Fixed
	- Start Date: 01/01/2018

- _End Point_
	- Mode: Fixed
	- End Date: 12/31/2018

**Q1 2017**
- _Start Point_
	- Mode: Fixed
	- Start Date: 01/01/2017

- _End Point_
	- Mode: Fixed
	- End Date: 03/31/2018

**Flow custom periods**

**6 Months**
- _Start Point_
	- Mode: Flow
	- Interval: Month
	- Offset: -5

- _End Point_
	- Mode: None

**Year to date**
- _Start Point_
	- Mode: Flow
	- Interval: Year
	- Offset: 0

- _End Point_
	- Mode: Flow
	- Interval: Day
	- Offset: 0

**Last Month**
- _Start Point_
	- Mode: Flow
	- Interval: Month
	- Offset: -1

- _End Point_
	- Mode: Flow
	- Interval: Month
	- Offset: 0

## Select Predefined Ranges
To select a predefined period, click the **Select Date Time Period** button (the ![wdd-range-filter-custom-period-icon](../../../../images/img125360.png) icon) in the Range Filter's [caption](../../dashboard-layout/dashboard-item-caption.md) and select the required period from the list.

![wdd-range-filter-select-custom-period](../../../../images/img125361.png)