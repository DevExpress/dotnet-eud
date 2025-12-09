---
title: Providing Maps
author: Natalia Kazakova
legacyId: 16613
---
# Providing Maps
This document explains how to use the default **DevExpress Dashboard maps**, or provide custom maps.

## Default Maps
DevExpress Dashboard ships with a set of default maps showing various parts of the world. The following maps are included.
* **World Countries** - a world map.
* **Europe** - a map of Europe.
* **Asia** - a map of Asia.
* **North America** - a map of North America.
* **South America** - a map of South America.
* **Africa** - a map of Africa.
* **USA** - a map of the USA.
* **Canada** - a map of Canada.

> [!NOTE]
> Note that the **World Countries** map has a lower level of detail than maps of specific regions and may not contain some countries. As an alternative, you can load a custom map with the required granularity.

To select the default map, use the **Default Map** button in the **Design** ribbon tab.

![Map_DefaultMaps_Ribbon](../../../../images/img22183.png)

As an alternative, use the corresponding command in the map's context menu.

## Custom Maps
DevExpress Dashboard uses a **Shapefile** vector format to provide custom maps. Commonly, this format includes two file types.
* **.shp** file - holds map shapes (points/lines/polygons).
* **.dbf** file - contains attributes for each shape.

To open an existing shapefile, use the **Load Map** or **Import Map** button in the Ribbon, or the command in the context menu (**Load Map...** or **Import Map...**).

![Map_LoadOpenMap_Ribbon](../../../../images/img22192.png)

In the invoked dialog, locate the required **.shp** file. Note that custom maps created in the Cartesian coordinate system are not supported.

> [!NOTE]
> If the map is opened using the **Load Map** button, the [dashboard XML definition](../../save-a-dashboard.md) will contain the path to a map shapefile. If the map is opened using the **Import Map** button, the dashboard XML definition will contain the map itself.

> [!NOTE]
> Attributes from the corresponding **.dbf** file located in the same directory will automatically be included in the map.