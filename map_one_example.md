**QGIS Walkthrough 1: A points map of listed buildings in Wales**

**Task**

- To build a points map using a downloaded shapefile and a base map, filter by a variable, and export as a html file

**Preparation**

- Install QGIS if you don’t have it. The work below was done with version 3.22

- Install the qgis2web plugins via: PLUGINS/MANAGE AND INSTALL PLUGINS

- Install extra base maps via: WEB/QUICKMAPSERVICES/SETTINGS/MORE SERVICES THEN “Get Contributed Pack”

**Start project & layout**

- Ensure the Layer Panel is visible: VIEW/PANELS/BROWSER

- Ensure the Data Source Manager, Map Navigation and Attributes toolbars are visible
  - VIEW/TOOLBARS/DATA SOURCE MANAGER
  - VIEW/TOOLBARS/MAP NAVIGATION
  - VIEW/TOOLBARS/ATTRIBUTES

- Open a New project (PROJECT/NEW) and save it in a folder of your choice (PROJECT/SAVE AS)

- Check the CRS that the project is using as default (PROJECT/PROPERTIES/CRS)

- Add a title to the project, which will become the ‘title’ in any html you make (PROJECT/PROPERTIES/GENERAL/PROJECT TITLE)

**Import files and assemble map**

- On the [LLE website](http://lle.gov.wales/catalogue/item/ListedBuildings/?lang=en), select the Downloads tab and download the *Listed Buildings* shapefile provided by Cadw

- Place the file in the directory you want to keep it in. If you move it after working with it the path files will be broken

- Examine the files inside the shapefile folder to see what is contained in the .SHP, .PRJ and .DBF files

- Import the shapefile into QGIS using
  - the Data Source Manager toolbar, or
  - LAYER/ADD LAYER/ADD VECTOR LAYER to locate the file locally via Source selector, or
  - Find the file in the Browser panel and double click to load

- In the Layers panel, right-click on the Cadw_ListedBuildingsMPoint file and select Properties. Under Information, the CRS is “OSGB 1936” and under Source it reads "OSGB 1936 / British National Grid"

- Add a base map: WEB/QUICK MAP SERVICES/OSM/OpenStreetMap Monochrome or ESRI Grey (light). Rename both layers if you wish

- The base map layer appears in the Layers panel. Just as a demonstration, reorder the layers to hide the points layer: note that the layers obscure each other. Adjust the opacity of the base map (PROPERTIES/TRANSPARENCY). Undo these steps

**Filter data and colour symbols**

- With a right-click on the Points layer select ‘Filter’. Select 'Grade' in Fields (upper left) then Sample or All in Values (upper right) to see what the different categories are for the ‘Grade’ variable attached to each data point. At the bottom of the dialogue box, write a SQL query to filter the data using a capital letter i and single quotes: "Grade" = 'I'

- Using the layer Properties (right-click) select the Symbology tab and adjust the colour and size of the points

- Using the Information tool on the Attributes toolbar click on a single point to see what information is attached.

**Save points layer as a separate file**

- Right-click on layer, then: EXPORT / SAVE FEATURES AS. Choose File Name and directory. Adjust CRS to ‘Project CRS’

**Export for web**

- WEB / QGIS2WEB / Create web map
- Under ‘Export’ choose a destination where it will be easy to locate the generated web files
