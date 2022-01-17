**QGIS Walkthrough 1: A points map of listed buildings in Wales**

**Task**

- To build a points map using a shapefile and a base map and publish it online.

**Preparation**

- Install QGIS if you don’t have it. The work below was done with version 3.22.

- Install the qgis2web plugins via: PLUGINS/MANAGE AND INSTALL PLUGINS

- Install extra base maps via: WEB/QUICKMAPSERVICES/SETTINGS/MORE SERVICES THEN “Get Contributed Pack”

**Layout**

- Ensure the Layer Panel is visible: VIEW/PANELS/BROWSER

- Ensure the Data Source Manager and Map Navigation toolbars are visible
  - VIEW/TOOLBARS/DATA SOURCE MANAGER
  - VIEW/TOOLBARS/MAP NAVIGATION
  - VIEW/TOOLBARS/MAP NAVIGATION
  - VIEW/TOOLBARS/ATTRIBUTES

- Open a New file (PROJECT/NEW) and save it in a folder of your choice (PROJECT/SAVE AS).

- Add a title to the project, which will become the ‘title’ in any html you make (PROJECT / PROPERTIES / GENERAL / PROJECT TITLE)

**Import files and assemble map**

- On the [LLE website](http://lle.gov.wales/catalogue/item/ListedBuildings/?lang=en), download the Listed Buildings shapefile provided by Cadw

- Place the file in the directory you want to keep it in. If you move it after working with it the path files will be lost.

- Examine the enclosed *Cadw_ListedBuildingsMPoint.prj* file using a text editor to see the projection: it refers to “OSGB 1936” and to “Transverse Mercator” and mentions several CRS codes: EPSG 7001, EPSG 6277, EPSG 8901, EPSG 4277, EPSG 9807, EPSG 27700. Close the file.

- Import the shapefile into QGIS using the Data Source Manager toolbar or LAYER/ADD LAYER/ADD VECTOR LAYER and locating the file locally using the Source selector.
In the Layers panel, right-click on the Cadw_ListedBuildingsMPoint file and select Properties / Information. The CRS is “OSGB 1936” and the ‘method’ is “Transverse Mercator”. Under Properties / Source check the “Assigned Coordinate Reference System”: it reads OSGB 1936 / British National Grid.

- Add a base map: WEB/QUICK MAP SERVICES / OSM / OpenStreetMap Monochrome

- The base map layer appears in the Layers panel. Reorder the layers to hide the points layer: note the layers obscure each other. Correct by placing the points layer uppermost.

- Right-click to open the base map’s properties and adjust ‘Global Opacity’ to 30%

**Filter data and colour symbols**

- With a right-click on the Points layer select ‘Filter’. Select Grade in Fields (upper left) then Sample or All in Values (upper right) to see what the different categories are for the ‘Grade’ variable attached to each data point. At the bottom of the dialogue box, write a SQL query to filter the data using a capital letter i and single quotes: "Grade" = 'I'

- Using the layer Properties (right-click) select the Symbology tab and adjust the colour.

- Using the Information tool on the Attributes toolbar click on a single point to see what information is attached.

**Save points layer as a separate file**

- Right-click on layer, then: EXPORT / SAVE FEATURES AS. Choose File Name and directory. Adjust CRS to ‘Project CRS’

**Export for web**

- WEB / QGIS2WEB / Create web map
- Under ‘Export’ choose a destination where it will be easy to locate the generated web files
