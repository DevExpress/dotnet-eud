---
title: Map Editor
author: Kseniya Kuzmina
---

# Map Editor
The Map Editor is a built-in tool that allows you to create and modify map items. You can also relocate map items on the map surface, rotate them using a rotation handle, and resize items using the sizing handles. The Map Editor's active mode determines which actions you can perform while editing the map. Use the corresponding editor panel buttons to switch between the Default, Transform, Edit and Create modes.

![Map Editor Preview](../../images/map-editor-preview.png)

## Map Editor's Panel

The Map Editor's panel consists of the following elements:

- ![Undo Button](../../images/map-editor-undo-button.png) - Cancels the last action.
- ![Redo Button](../../images/map-editor-redo-button.png) - Restores the last canceled action.
- ![Default Mode Button](../../images/map-editor-default-mode-button.png) - Enables Default mode.
- ![Transform Mode Button](../../images/map-editor-transform-mode-button.png) - Activates Transform mode.
- ![Edit Mode Button](../../images/map-editor-edit-mode-button.png) - Turns on Edit mode.
- ![Add Pushpin Button](../../images/map-editor-add-pushpin-button.png) - Enables "Create Pushpin" mode to create pushpins.
- ![Add Path Button](../../images/map-editor-add-path-button.png) - Enables "Create Path" mode to create map paths.
- ![Add Polyline Button](../../images/map-editor-add-polyline-button.png) - Activates "Create Polyline" mode to create map polylines.
- ![Add Dot Button](../../images/map-editor-add-dot-button.png) - Enables "Create Dot" mode to create map dots.
- ![Add Ellipse Button](../../images/map-editor-add-ellipse-button.png) - Enables "Create Ellipse" mode to create ellipses.
- ![Add Rectangle Button](../../images/map-editor-add-rectangle-button.png) - Turns on "Create Rectangle" mode to create map rectangles.
- ![Add Line Button](../../images/map-editor-add-line-button.png) - Enables "Create Line" mode to create map lines.

## Map Editor Modes

The Map editor provides the following modes that define the available actions when editing the map:

### Default Mode

You can only view the map and cannot to edit, create and transform map items when the Default mode is enabled. You can use the ![Default Mode Button](../../images/map-editor-default-mode-button.png) button to turn on this mode. 

### Transform Mode

Select the ![Transform Mode Button](../../images/map-editor-transform-mode-button.png) symbol to enable the Transform mode. This mode allows you to resize and rotate the selected map items using the sizing and rotation handles that appear when selecting items. You can also move map items by dragging them to the desired location.

![Item Transformation](../../images/map-editor-transformation-in-action.png)

### Edit Mode

Use the ![Edit Mode Button](../../images/map-editor-edit-mode-button.png) button to enable the Edit mode. It allows you to move, add, and remove item vertices to change vector map shapes. To edit a map item in this mode, select an item to display its points and perform one of the following actions:

|Action|Animation|Description|
|---|---|---|
|Moving vertices|![Moving Vertices](../../images/map-editor-moving-points.gif)|Relocates an existing map shape's point by dragging it to a new position.|
|Adding vertices|![Adding Vertices](../../images/map-editor-adding-points.gif)|To add a new vertex, hover the mouse pointer over the item's edge between two neighbor points and click where you want to insert a new vertex.|
|Removing vertices|![Removing Vertices](../../images/map-editor-removing-points.gif)|Removes a map shape's point by double-clicking it.|

Note that you can only edit the following map vector items:
- Map line
- Map path
- Map polygon
- Map polyline

### Create Mode

Create mode allows you to add new items to the map. Select one of the following symbols to create map items: ![Add Pushpin Button](../../images/map-editor-add-pushpin-button.png) ![Add Path Button](../../images/map-editor-add-path-button.png) ![Add Polyline Button](../../images/map-editor-add-polyline-button.png) ![Add Dot Button](../../images/map-editor-add-dot-button.png) ![Add Ellipse Button](../../images/map-editor-add-ellipse-button.png) ![Add Rectangle Button](../../images/map-editor-add-rectangle-button.png) ![Add Line Button](../../images/map-editor-add-line-button.png)

You can add dots and pushpins by clicking at the required location. To create a complex map item, sequentially add points to form a map item. The following animation shows how to create a map path:

![Map Editor Create Mode](../../images/map-editor-creating-path.gif)