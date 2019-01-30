---
title: " Getting Started with QGIS "
date: "2018-12-23"
description: "How to Install QGIS in Ubuntu"
disable_comments: false # Optional, disable Disqus comments if true
authorbox: true # Optional, enable authorbox for specific post
toc: false # Optional, enable Table of Contents for specific post
draft: false
mathjax: true # Optional, enable MathJax for specific post
categories:
  - "GIS"
tags:
  - "QGIS"
---

### In this post we will learn the following skills

+ Launching QGIS
+ Loading Raster and Vector Layers
+ Saving Projects
+ Understanding the QGIS User Interface

Required Data : [ All Resource for Workshop ](all-resources.zip)

Download the all-resources directory and extract in the home directory

### Activity 1 : Add Vector Layer
    - Open New QGIS project
    - From Menu Layer >> Add Layer >> Add Vector Layer >> From Source Vector Dataset Select Maharashtra_water directory and select `maharashtra_water.shp` file
    - From the Layers menu, Right Click and Select Zoom to Layer option
    - From the Layer >> Data Source Manager >> Browser >> XYZ Tiles >> Select OpenStreetMap
    - From the Layer menu drag the OpenStreetMap layer to down
    - Right Click the Maharashtra_water Layer and Open attribute table
    - Save project it will be saved as `.qgs` file


![ Maharashtra Water ](maharashtra_water.png)


  From the Layers menu right click and open Attribute tables

![ Maharashtra Water Attribute Table ](maharashtra_water_attr.png)


`Remember that layer order matters !`


### Activity 2: Add Raster Layer
    - First Extract the NE1_LR_LC.zip file
    - From From Menu Layer >> Add Layer >> Add Raster Layer >> From Source Raster Dataset Select the `NE1_LR_LC.tif` file

![ Natural Earth Land Cover Data ](naturalEarthData.png)

+ If you want to save the layers as .sh in ESRI file format, You select any layer and from layer option > Save as >> Select ESRI shape file

### Activity 3: Explore the User Interface of the QGIS

Use Dashboard or QGIS icon to Launch QGIS. To close use can use X icon or `Project` Menu and `Exit QGIS` option When you start QGIS it will open following user interface

![ QGIS User Interface ](userInterface.png)

The QGIS GUI is divided into five components:

  + **Menu Bar**: Standard Menu providing all QGIS features
  + **Toolbars** : Tools for interacting with the map, `right click` on toolbars to on/off toolbar for specific function
  + **Panels**: Special widgets that you can interact, see info, logs etc and perform complex tasks
  + **Map View**: or Map canvas here maps are displayed, zoom in, zoom out and interact with the map
  + **Status Bar**: General information about the map view, and actions processed, Map Coordinates, CRS etc is displayed

### Menu Bar
  + **Project** : Create, Save, Open projects, set Project properties, Print Layout and Making Report
  + **Edit** : Editing tools for used while making the map
  + **View** : Zoomming, Measure Areas, Bookmarks and Hide/Show Layers
  + **Layer**: Data Source Manager, Create/Add Layers, Enable layer editing, Save Layers and different files formats, Set CSRs to layers and see and edit attribute tables
  + **Setting** : QGIS Settings, User profiles, Style manager and the keyboard shortcuts
  + **Plugins** : Install/Uninstall plugins and python console
  + **Vector** : All vector processing and analysis tools
  + **Raster** : Various raster analysis tools
  + **Database**: Databse management
  + **Web**: Meta data
  + **Processing** : Processing toolbox
  + **Help**: Help documentation, Cerdits, QGIS version etc
