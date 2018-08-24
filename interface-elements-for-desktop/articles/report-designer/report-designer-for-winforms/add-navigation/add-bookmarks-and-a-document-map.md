---
title: Add Bookmarks and a Document Map
---
# Add Bookmarks and a Document Map

This document describes how to use bookmarks for mapping the report elements' hierarchy to the Document Map that is displayed in a Print Preview, and speeds up the navigation through complex reports.

The example below is based on the following report:

![eurd-win-add-bookmark-source-report](../../../../images/eurd-win-add-bookmark-source-report.png)

This report displays products that are [grouped](..\shape-report-data\group-and-sort-data\group-data.md) by the **CategoryName** field. 

The following image illustrates the resulting report with a hierarchical Document Map. Clicking any bookmark navigates the Print Preview to the document section containing the associated element.

![eurd-win-addbookmark_result](../../../../images/eurd-win-addbookmark_result.png)

Use the following steps to generate a Documnet Map in your grouped report.

1. Select the label placed in the **Group Header** band and switch to the [Property Grid](..\report-designer-tools\ui-panels\property-grid.md)'s **Expressions** tab. Click the **Bookmark** property's ellipsis button, and in the invoked **Expression Editor**, select the **CategoryName** data field.
	
	![eurd-win-addbookmark-set-bookmark-for-group](../../../../images/eurd-win-addbookmark-set-bookmark-for-group.png)
	
	In the legacy binding mode (if the Property Grid does not provide the **Expressions** tab), you can specify this property in the Property Grid's **DataBindings** category.
	
	![eurd-win-addbookmark_legacy](../../../../images/eurd-win-addbookmark_legacy.png)
2. In the same way, select the label in the **Detail** band and bind its **Bookmark** property to the **ProductName** data field.
	
	![eurd-win-addbookmark-set-bookmarks-for-details](../../../../images/eurd-win-addbookmark-set-bookmarks-for-details.png)
	
	Most of the reporting controls (for example, [Table](..\use-report-elements\use-tables.md), TableCell, [CheckBox](..\use-report-elements\use-basic-report-controls\check-box.md), etc.) supports the **Bookmark** property.
3. Set the same label's **BookmarkParent** property to the label in the group band. This arranges bookmarks into a parent-child structure reflecting the report elements' hierarchy in the Document Map.
	
	![eurd-win-addbookmark-bookmark-parent](../../../../images/eurd-win-addbookmark-bookmark-parent.png)
	
	> [!NOTE]
	> Avoid cyclic bookmarks that occur when you assign two bookmarks as parents to each other. In this scenario, an exception raises when you attempt to create the report document.
4. Select the report itself and assign text to its **Bookmark** property to determine the root node's caption in the **Document Map**.
	
	![eurd-win-addbookmark-root-bookmark](../../../../images/eurd-win-addbookmark-root-bookmark.png)
	
	The root bookmark displays the report name if you do not specify this property.

> [!NOTE]
> Duplicated bookmarks are suppressed to prevent adding multiple bookmarks with the same name to a final document. You can disable the  report's **BookmarkDuplicateSuppress** property to allow duplicated bookmarks.