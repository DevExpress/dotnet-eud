---
title: Create a Table Report
author: Eugeniy Burmistrov
legacyId: 12455
---
# Create a Table Report
This tutorial will guide you through the process of creating a **Table Report**, and printing and saving it to your hard drive.
 The table report is a data-aware **Snap** report with a tabular master-detail layout.

To get started with this tutorial, create a new Snap document and provide a hierarchical data source for it, as described in the [Create a Master-Detail Data Source](../connect-to-data/create-a-master-detail-data-source.md) topic.

To create a master-detail Snap document layout, do the following.
1. Create a simple tabular report by selecting the data fields that you wish to include in the report in the [Data Explorer](../graphical-user-interface/snap-application-elements/data-explorer.md) and dragging them to the [Design Surface](../graphical-user-interface/snap-application-elements/design-surface.md). When you drop data fields onto the empty space in the document body, they are added as columns of a table. You can select multiple data fields by pressing **CTRL** or **SHIFT**.
	
	![snap-getting-started-tabular-report01](../../../images/img22836.png)
	
	To improve performance, Snap shows only the first **20** data rows of a Snap list by default. To change this setting, use the **Editor Row Limit** option, which is located on the [List](../graphical-user-interface/main-toolbar/data-tools-list.md) tab of the main toolbar.
	
	![SnapControl-get-started-10](../../../images/img18228.png)
2. To convert the layout of a Snap list to a paragraph presentation, select the Snap list you wish to convert and click the **Convert to Paragraphs** command in the **List** tab of the contextual **Data Tools** toolbar category. Note that there is no reverse action allowing you to convert a Snap list back to the tabbed form.
	
	![snap-getting-started-tabular-report04](../../../images/img22839.png)
	
	The report should now appear as shown in the following image.
	
	![snap-getting-started-tabular-report02](../../../images/img22837.png)
	
	To remove a list header, select the Snap list, click the **Header** command in the **List** tab of the main toolbar, and select **Remove Header** in the invoked drop-down menu.
	
	![snap-getting-started-tabular-report03](../../../images/img22838.png)
3. To create a detail report, drag data fields from the child data table in the **Data Explorer** onto the lower border of the master report's data row, as shown in the image below.
	
	![snap-getting-started-tabular-report05](../../../images/img22840.png)
	
	The added detail part will have a tabular form by default.
	
	![snap-getting-started-tabular-report06](../../../images/img22841.png)
4. To preview your Snap document click the **Print Preview** button in the [General Tools: File](../graphical-user-interface/main-toolbar/general-tools-file.md) tab of the main toolbar.
	
	![snap-getting-started-tabular-report07](../../../images/img22842.png)