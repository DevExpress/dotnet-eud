---
title: Search Panel
author: Anna Kondratova
---
# Search Panel

Use the Search Panel to locate data and highlight search result by typing the filter criterion in the search box.

![SearchPanel](../../../images/img17905.png)

## Apply the Search Panel Filter Criterion

Press Enter or click the **Search** button to apply a filter criterion typed in the search panel. Otherwise, a filter is automatically applied in 1.2 seconds.

## Clear the Search Panel Filter Criterion
To clear the search panel filter criterion, do one of the following:
* Press Delete or Backspace.
* Click the **Clear** button.
* Click the clear button in the search box when it is focused and not empty.
	
	![EUD_Grid_SearchPanel](../../../images/img25472.png)

## Search syntax
A search criterion consists of a single word in its simplest form. However, the search panel allows creating composite criteria.
* **Mask:** criterion 
	
	 maria
	
	![EUD_Grid_SearchPanelCriterion1](../../../images/img25474.png)
	
	**Example description:** selects records that contain the "maria" string in any search column.
* **Mask:** column:criterion 
	
	contact:maria
	
	![EUD_Grid_SearchPanelCriterion2](../../../images/img25475.png)
	
	You can search against a specific column by preceding a search string with the column's caption plus a colon character. Instead of the complete caption, it is possible to use the caption's initial characters to perform a search against the first column whose name starts with the specified substring. To search against a column whose caption contains space characters, specify the column's display caption in quotation marks.
	
	If the search string contains multiple conditions separated by space characters, and at least one condition defines a search against a specific column, the tree list displays only records that match all of these conditions (the AND logical operator combines conditions).
	
	**Example description:** selects records that contain "maria" in the column that starts with "contact".
* **Mask:** criterion1 criretion2 
	
	maria anders
	
	**Option AND**
	
	![EUD_Grid_SearchPanelCriterion3_v2](../../../images/img25993.png)
	
	**Option OR**
	
	![EUD_Grid_SearchPanelCriterion3](../../../images/img25476.png)
	
	Based on conditions provided by your application vendor, the search panel can search words separated by space characters in one of the following ways.
	
	**Option AND**
	
	Only records that match all of the conditions are shown (that is, the conditions are combined by the AND logical operator).
	
	**Example description:** selects records that contain both "maria" AND "anders" strings in any search column.
	
	**Option OR**
	
	If there is no column specification, the tree list displays records that match at least one of these conditions (the OR logical operator combines the conditions).  If at least one condition defines a search against a specific column, the tree list displays only records that match all of these conditions (the AND logical operator combines the conditions).
	
	**Example description:** selects records that contain either "maria" OR "anders" strings in any search column.
* **Mask:** "criterion with spaces" 
	
	"maria anders"
	
	![EUD_Grid_SearchPanelCriterion4](../../../images/img25477.png)
	
	Specify this string in quotation marks to search for a string containing a space character.
	
	**Example description:** selects records that contain "maria anders" in any search column.
* **Mask:** criterion1 -criterion2
	
	maria -anders
	
	![EUD_Grid_SearchPanelCriterion5](../../../images/img25478.png)
	
	Precede a condition with "-" to exclude records that match this condition from the resulting set. There should be no space between the "-" sign and the condition.
	
	**Example description:** selects records that contain "maria", excluding records that contain "anders".
* **Mask:**
	
	 criterion1 +criterion2 
	
	maria +sweden
	
	![EUD_Grid_SearchPanelCriterion6](../../../images/img25479.png)
	
	Precede a condition with "+" to display only records that match this condition. The "+" specifier allows implementing the logical AND operator. There should be no space character between the "+" sign and the condition.
	
	**Example description:** selects records that contain both "maria" AND "sweden" in search columns.
