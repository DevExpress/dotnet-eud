---
title: Creating Parameters
author: Polina Tuyreva
---
# Cascading Parameters

Create cascading parameters to filter a list of predefined parameter values based on another parameter's values. The following image illustrates cascading parameters where the **pProducts** parameter values are filtered by the selected category:

![Dashboard for WinForms - Cascading Parameters](~/images/cascading-parameters-winforms.gif)

In case of two parameters, the first parameter is used to filter the data source for the second parameter with [dynamic list](creating-parameters.md#dynamic-list) settings.

## Create Cascading Parameters

The dashboard in this example is connected to a Northwind database (an SQL Database) and contains three [queries](work-with-data/manage-sql-queries.md): *Categories*, *Products*, and *OrderReports*. The Grid item visualizes data from the *OrderReports* query.

In this tutorial, you will create two dashboard parameters: 
* The **pCategory** parameter filters the *Products* query. The *Products* query is a data source for the **pProducts** parameter. 
* The **pProducts** parameter filters the *OrderReports* query.  

The steps below create cascading parameters in the WinForms Dashboard Designer:

1. Create a dashboard parameter called **pCategory** with dynamic list settings. Use the *Categories* query as a data member and the *CategoryID* as a value member. 

    The parameter settings may look as follows:

    ![Dashboard for WinForms - Create Dashboard Parameter](~/images/category-parameter-cascading.png)

2. Use the created **pCategory** parameter to [filter](work-with-data/filter-queries.md) the *Products* query. 
   
   To do this, invoke the [Query Builder](work-with-data/using-the-query-builder.md) and click the **Filter...** button to specify the filter criteria in the **Filter Editor**. Choose the **Bind To** option to automatically bind a [query parameter](work-with-data/pass-query-parameters.md) to the created dashboard parameter:

    ![Dashboard for WinForms - Filter Query](~/images/category-parameter-filter-cascading.png)

    The resulting query looks as follows: 

    ```
    [Products.CategoryID]=?pCategory
    ```

3. Create a dashboard parameter called **pProducts** with dynamic list settings. Use the *Products* query as a data member and the *ProductID* as a value member.

    The parameter settings may look as follows:

    ![Dashboard for WinForms - Create Dashboard Parameter](~/images/products-parameter-cascading.png)
    

4. Use the **pProducts** dashboard parameter to filter the *OrderReports* query.

    To do this, invoke the [Query Builder](work-with-data/using-the-query-builder.md) and click the **Filter...** button to specify the filter criteria in the **Filter Editor**. Choose the **Bind To** option to automatically bind a [query parameter](work-with-data/pass-query-parameters.md) to the created dashboard parameter:

    ![Dashboard for WinForms - Filter Queries](~/images/products-parameter-filter-cascading.png)

    The resulting query looks as follows: 
    
    ```
    [OrderReports.ProductID] In ?pProducts
    ```

5. Create a Grid item to visualize data from the filtered *OrderReports* query.

>[!TIP]
>When using a [multi-value](creating-parameters.md#allow-multiselect) parameter to filter a query, create the condition with the `Is any of` or `Is none of` operator. 
