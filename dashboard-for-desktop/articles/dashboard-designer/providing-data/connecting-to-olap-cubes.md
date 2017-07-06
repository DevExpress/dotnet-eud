---
title: Connecting to OLAP cubes
---
# Connecting to OLAP cubes
The Dashboard Designer provides the capability to connect to an OLAP cube in the Microsoft Analysis Services database using the **Data Source** wizard.

To connect to an OLAP cube in the Dashboard Designer, do the following steps.
1. Click the **New Data Source** button in the **Data Source** ribbon tab.
	
	![DataBinding_NewDataSource](../../../images/Img18472.png)
2. On the first page of the invoked **Data Source Wizard** dialog, select **Olap** and click **Next**.
	
	![DataSourceWizard_DataSourceType_Olap](../../../images/Img120680.png)
3. On the next page, choose the required **Connection type**. The following types are available.
	* [Server](#server)
	* [Local cube file](#local-cube-file)
	* [Custom connection string](#custom-connection-string)

## <a name="server"/>Server
If you selected **Server**, the following options are available.

![DataSourceWizard_OlapServer](../../../images/Img118049.png)
* **Server name**
	
	Specify the name of the OLAP server to which the connection should be established.
* **UserId**
	
	Specify the user name used to authenticate to the OLAP server.
* **Password**
	
	Specify the password used to authenticate to the OLAP server.
* **Catalog**
	
	Select a data catalog that contains cubes.
* **Cube Name**
	
	Select a cube that provides OLAP data.

Click **Finish** to create a data source.

## <a name="local-cube-file"/>Local Cube File
If you selected **Local cube file**, specify the path to the requiredOLAP cube. To locate the cube, click the ellipsis button next to the Database field.

![DataSourceWizard_OlapLocalFile](../../../images/Img118050.png)

Click **Finish** to create a data source.

## <a name="custom-connection-string"/>Custom Connection String
If you selected **Custom connection string**, specify a connection string in the **Custom connection string** editor.

![DataSourceWizard_CustomString](../../../images/Img118051.png)

Click **Finish** to create a data source.