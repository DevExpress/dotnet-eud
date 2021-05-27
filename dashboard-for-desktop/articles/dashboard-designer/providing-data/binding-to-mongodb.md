---
title: Binding to MongoDB
author: Margarita Zakhodyaeva
---
# Binding to MongoDB

The WinForms Designer allows you to connect to MongoDB in the Data Source Wizard. 

> [!NOTE]
> The [MongoDB.Driver](https://www.nuget.org/packages/MongoDB.Driver) package should be installed in your project to supply MongoDB data at runtime.

Follow the steps below to establish a connection to a database:

1. Click the **New Data Source** button in the **Data Source** ribbon tab.
	
    ![DataBinding_NewDataSource](../../../images/img18472.png)
2. On the first page of the invoked **Data Source Wizard** dialog, select **MongoDB** and click **Next**.

	![Data Source Wizard DataBase MongoDB](~/images/win-data-source-wizard-database-mongodb.png)
    
3. Specify connection parameters on the next page. You can pass an entire string or enter connection fields individually. Refer to the following topic for information about connection string format and options: [Connection String URI Format](https://docs.mongodb.com/manual/reference/connection-string/).

    >[!ImageGallery]
    >![MongoDB Connection String](~/images/win-data-source-wizard-mongo-specify-connection-parameters.png)
    >![MongoDB Individual Connection Fields](~/images/win-data-source-wizard-database-mongodb-individual.png)

4. The following page allows you to configure queries. Select databases and collections that you want to load from the MongoDB instance. A string stored in a query's **Collection** column is the default name for the query. The names of MongoDB queries should be unique. You can use the **Alias** column to set unique names for queries in the same collection. To filter queries, add a filter string to the **Filter** column.

    ![Data Source Wizard MongoDB specify quueries](~/images/win-data-source-wizard-mongodb-specify-queries.png) 