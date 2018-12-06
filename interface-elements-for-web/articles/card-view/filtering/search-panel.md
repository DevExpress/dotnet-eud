---
title: Search Panel
author: Anna Kondratova
legacyId: 115292
---
# Search Panel
Type a filter criterion in the search panel to filter data and highlight search results.

![ASPxCardView_Seraching](../../../images/img118489.png)

## Apply the Search Panel Filter Criterion
To apply a filter criterion typed in the search panel, press the ENTER key or click the **Search** button. Otherwise, a filter is automatically applied in 1.2 seconds.

## Clear the Search Panel Filter Criterion
To clear the search panel filter criterion, do one of the following.
* Press DELETE or BACKSPACE.
* Click the **Clear** button.
* Click the clear button that is displayed within the editor when the editor is focused and is not empty.
	
	![EUD_Grid_SearchPanel](../../../images/img25472.png)

## Search syntax
In its simplest form, a search criterion consists of a single word. However, the search panel allows you to create composite criteria.
* **Mask:** criterion 
	
	**Example:** carlos
	
	![ASPxCardView_Searching_OneWord](../../../images/img118686.png)
	
	**Example description:** selects records that contain the "carlos" string in any search column.
* **Mask:** column:criterion
	
	**Example:** city:san
	
	![ASPxCardView_Searching_Column](../../../images/img118689.png)
	
	You can search against a specific column by preceding a search string with the column's caption and a colon character. Instead of the complete caption, it is possible to use the initial characters of the caption. A search will be performed against the first column whose name starts with the specified substring. If you want to search against a column whose caption contains space characters, specify the column's display caption in quotation marks.
	
	If the search string contains multiple conditions separated by space characters, and at least one condition defines a search against a specific column, only records that match all of these conditions are shown (i.e., the conditions are combined by the AND logical operator).
	
	**Example description:** selects records that contain "san" in the column that starts with "city".
* **Mask:** criterion1 criterion2 
	
	**Example:** carlos venezuela
	
	**Option 1**
	
	![ASPxCardView_Searching_And](../../../images/img118687.png)
	
	**Option 2**
	
	![ASPxCardView_Searching_Or](../../../images/img118688.png)
	
	Based on conditions provided by your application vendor, the search panel can search words separated by space characters in one of the following ways.
	
	**Option AND**
	
	Only records that match all of the conditions are shown (i.e., the conditions are combined by the AND logical operator).
	
	**Example description:** selects records that contain both "carlos" AND "venezuela" strings in any search column.
	
	**Option OR**
	
	If there is no column specification, records that match at least one of these conditions are shown (i.e., the conditions are combined by the OR logical operator). If at least one condition defines a search against a specific column, only records that match all of these conditions are shown (i.e., the conditions are combined by the AND logical operator).
	
	**Example description:** selects records that contain either "carlos" OR "venezuela" strings in any search column.
* **Mask:** "criterion with spaces"
	
	**Example:** "maria anders"
	
	![ASPxCardView_Searching_Quotation](../../../images/img118690.png)
	
	If you want to search for a string containing a space character, specify this string in quotation marks.
	
	**Example description:** selects records that contain "maria anders" in any search column.
* **Mask:** criterion1 -criterion2
	
	**Example:** maria -anders
	
	![ASPxCardView_Searching_Exclude](../../../images/img118691.png)
	
	Precede a condition with "-" to exclude records that match this condition from the resulting set. There should be no space between the "-" sign and the condition.
	
	**Example description:** selects records that contain "maria", excluding records that contain "anders".
* **Mask:** criterion1 +criterion2
	
	**Example:** Spain +Madrid
	
	![ASPxCardView_Searching_Include](../../../images/img123943.png)
	
	Precede a condition with "+" to display only records that match this condition. The "+" specifier allows you to implement the logical AND operator. There should be no space character between the "+" sign and the condition.
	
	**Example description:** selects records that contain both "Spain" AND "Madrid" in search columns.