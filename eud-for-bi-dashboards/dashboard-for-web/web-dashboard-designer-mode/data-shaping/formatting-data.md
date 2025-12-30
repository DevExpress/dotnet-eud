---
title: Formatting Data
author: Natalia Kazakova
legacyId: 117708
---
# Formatting Data
The Web Dashboard allows you to customize various format settings for numeric and date-time values.
* [Formatting Numeric Values](#numeric)
* [Formatting Date-Time Values](#datetime)
* [Currency Formatting Specifics](#currency)

## <a name="numeric"/>Formatting Numeric Values
To specify a format for numeric values, open the dashboard item [Bindings](../ui-elements/dashboard-item-menu.md) menu, select a required data item and go to the **Format** section.

![wdd-format-rype](../../images/img125536.png)

In the **Format type** field, select the required format type.

| Format Type | Description |
|---|---|
| **Auto** | Format settings are automatically determined based on the data type. |
| **General** | Converts a number to the most compact of either fixed-point or scientific notation, depending on the type of the number. |
| **Number** | Converts a number to a string of the "-d,ddd,ddd.ddd…" form where "-" indicates a negative number symbol (if required), "d" indicates a digit (0-9), "," indicates a group separator, and "." indicates a decimal point symbol. |
| **Currency** | Converts a number to a string that represents a currency amount. To learn about currency formatting specifics, see the [Currency Formatting Specifics](#currency) section of this document. |
| **Scientific** | Converts a number to a string of the "-d.ddd…E+ddd" or "-d.ddd…e+ddd" form where each "d" indicates a digit (0-9). |
| **Percent** | Multiplies a number by 100 and converts it to a percentage string. |

Other format settings are in effect for only specific format types.

| Setting | Description | Format Types |
|---|---|---|
| **Unit** | The unit to which values should be converted. | Number, Currency |
| **Precision** | The number of fractional digits that should be displayed. | Scientific, Percent |
| **Include group separator** | Specifies whether or not separators should be inserted between digit groups. | Number, Currency, Percent |
| **Currency** | Defines the currency sign and format settings that should be used to display currency values. To learn about currency formatting specifics, see the [Currency Formatting Specifics](#currency) section of this document. | Currency |

## <a name="datetime"/>Formatting Date-Time Values
To specify a format for date-time values, use the **Format Type** option in the data item's **Format** section.

![wdd-format-type-date-time](../../images/img124765.png)

> [!NOTE]
> Specific group intervals do not have format options. This means that corresponding values can only be presented in a single manner. The **Format** section is not displayed for such group intervals.

The following list shows format types by group interval.
* Year
	* _Full_ - The full year pattern (Example - 6&#47;15&#47;2017 1:45:30 PM -&gt; 2017 (en-US)).
	* _Abbreviated_ - The year from 00 to 99 (Example - 6&#47;15&#47;2017 1:45:30 PM -&gt; 17 (en-US)).
* Quarter
	* _Full_ - The full quarter pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Q2 (en-US)).
	* _Numeric_ - The quarter from 1 through 4 (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 2 (en-US)).
* Month
	* _Full_ - The full name of the month (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; June (en-US)).
	* _Abbreviated_ - The abbreviated name of the month (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Jun (en-US)).
	* _Numeric_ - The month from 1 through 12 (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6 (en-US)).
* Hour
	* _Long_ - Long hour pattern, 12-hour format (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 1:00 PM).
	* _Short_ - Short hour pattern, 24-hour format (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 13).
* Day of Week
	* _Full_ - The full name of the day of the week (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday (en-US)).
	* _Abbreviated_ - The abbreviated name of the day of the week (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Mon (en-US)).
	* _Numeric_ - The day of the week from 1 through 7 (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 2 (en-US)).
* Day-Month-Year
	* _Long_ - Long date pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday, June 15, 2017 (en-US)).
	* _Short_ - Short date pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6&#47;15&#47;2017 (en-US)).
* Date-Hour
	* _Long_ - Long date pattern, long hour pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday, June 15, 2017 1:00 PM (en-US)).
	* _Short_ - Short date pattern, long hour pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6&#47;15&#47;2017 1:00 PM (en-US)).
	* _Time only_ - Long hour pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 1:00 PM (en-US)).
* Date-Hour-Minute
	* _Long_ - Long date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday, June 15, 2017 1:45 PM (en-US)).
	* _Short_ - Short date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6&#47;15&#47;2017 1:45 PM (en-US)).
	* _Time only_ - Long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 1:45 PM (en-US)).
* Date-Hour-Minute-Second
	* _Long_ - Long date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday, June 15, 2017 1:45:30 PM (en-US)).
	* _Short_ - Short date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6&#47;15&#47;2017 1:45:30 PM (en-US)).
	* _Time only_ - Long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 1:45:30 PM (en-US)).

The list below illustrates format types related to the **Exact Date** group interval.
* Year
	* _Full_ - The full year pattern (Example: 6/15/2017 1:45:30 PM -> 2017 (en-US)).
	* _Abbreviated_ - The year from 00 to 99 (Example: 6/15/2017 1:45:30 PM -> 17 (en-US)).
* Quarter
	* _n/a_ - The default year and full quarter pattern (Example: 6/15/2017 1:45:30 PM -> Q2 2017 (en-US)).
* Month
	* _n/a_ - The default year pattern and the full name of the month (Example: 6/15/2017 1:45:30 PM -> June, 2017 (en-US)).
* Day
	* _Long_ - Long date pattern (Example: 6/15/2017 1:45:30 PM -> Monday, June 15, 2017 (en-US)).
	* _Short_ - Short date pattern (Example: 6/15/2017 1:45:30 PM -> 6/15/2017 (en-US)).
* Hour
	* _Long_ - Long date pattern, long time pattern (Example: 6/15/2017 1:45:30 PM -> Monday, June 15, 2017 1:00 PM (en-US)).
	* _Short_ - Short date pattern, long time pattern (Example: 6/15/2017 1:45:30 PM -> 6/15/2017 1:00 PM (en-US)).
	* _Time only_ - Long time pattern (Example: 6/15/2017 1:45:30 PM -> 1:00 PM (en-US)).
* Minute
	* _Long_ - Long date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday, June 15, 2017 1:45 PM (en-US)).
	* _Short_ - Short date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6&#47;15&#47;2017 1:45 PM (en-US)).
	* _Time only_ - Long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 1:45 PM (en-US)).
* Second
	* _Long_ - Long date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; Monday, June 15, 2017 1:45:30 PM (en-US)).
	* _Short_ - Short date pattern, long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 6&#47;15&#47;2017 1:45:30 PM (en-US)).
	* _Time only_ - Long time pattern (Example: 6&#47;15&#47;2017 1:45:30 PM -&gt; 1:45:30 PM (en-US)).

## <a name="currency"/>Currency Formatting Specifics
The Web Dashboard allows you to specify currency formats for the current data item or for entire dashboard.
* To set a data item currency format, open the dashboard item [Bindings](../ui-elements/dashboard-item-menu.md) menu, select a required data item and go to the **Format** section. Select **Currency** as a format type and specify the required culture using the **Currency** combo box.
	
	![wdd-format-type-currency](../../images/img126159.png)
	
	You can also specify the data item to use the client culture. For this, select the _Use client system settings_ in the combo box.
* To set the dashboard currency, open the [dashboard menu](../ui-elements/dashboard-menu.md) and go to the **Currency** page. Here you can select the required currency from the list.
	
	![wdd-format-type-currency-entire-dashboard](../../images/img124766.png)
	
	You can also specify the dashboard to use the client culture. For this, select the _Use client system settings_ item.