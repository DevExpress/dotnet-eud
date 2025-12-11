---
title: Create Drill-Through Reports
---
# Create Drill-Through Reports

Follow this tutorial to create a _drill-through report_ (a user can click a Category entry to invoke a detail report with Products). This report type keeps the original report compact while still allowing access to more detailed information. 

The tutorial involves two main steps:

- Add a master-detail relationship between "Categories" and "Products" reports within one project. 
- Use detail report parameters to filter records based on the selected category.

## Add a Master-Detail Relationship between Reports

Define a master-detail relationship between _Category_ and _Product_ reports within a single project:

- Select the XRControl's element (**Table Cell** in this example) in the main report.
- Set its **Action** property to **Navigate to Report**.
- Assign the **Report Source URL** property to a detail report instance.

![Specify the Navigate to Report action](../../../images/web-specify-navigate-to-report-action.png)

If you switch to **Preview**, you can click on a _Category_ value in the table. The **Preview** window navigates to the detail report that contains all _Product_ entries. The next step explains how to filter this list. 

![Drill-Through report preview](../../../images/web-detail-report-navigation.png)

You can click "Categories Report" below the Document Viewer toolbar and navigate back to the original report.

![Breadcrumb navigation](../../../images/web-breadcrumb-control-navigation.png)

## Specify Parameter Binding to Display Required Data

You can specify parameters during detail report navigation. Use the **Parameter Bindings** property to limit displayed records (such as products) to a selected category.

Click the **Parameter Bindings** property and select the detail report parameter. Set **Binding** to the data field or parameter of the original report. In this example, **Binding** is set to the _CategoryID_ field.

![Specify Parameter Binding](../../../images/web-specify-binding.png)

Set the following filter string in the detail report to display product records for the selected category.

![Set filter string](../../../images/web-set-filter-string.png)

## Result

Switch to **Preview** and click on a category entry in the master report. The **Preview** navigates to the detail report that displays only products related to the selected category.

![Drill-Through report](../../../images/web-drill-through-result.png)



  
