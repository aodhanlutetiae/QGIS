**QGIS Walkthrough 1: A points map of listed buildings in Wales**

**Task**

- Build a points map using a downloaded shapefile and a base map, filter by a variable, and export as a web page

**Start project & layout**

- Ensure the Layer Panel is visible: VIEW / PANELS / Layers

- Ensure the Data Source Manager, Map Navigation and Attributes toolbars are visible
  - VIEW / TOOLBARS / DATA SOURCE MANAGER
  - VIEW / TOOLBARS / MAP NAVIGATION
  - VIEW / TOOLBARS / ATTRIBUTES

- Open a New project (PROJECT/NEW) and save it in a folder of your choice (PROJECT / SAVE AS)

- Check the CRS that the project is using as default (PROJECT / PROPERTIES / CRS)

**Import files and assemble map**

- On the [Welsh government map site](https://datamap.gov.wales/layers/inspire-wg:Cadw_ListedBuildings), download the *Listed Buildings* zipped shapefile provided by Cadw, or [the protected wrecks dataset](https://datamap.gov.wales/layers/inspire-wg:Cadw_DesignatedWrecks)

- Place the file in the directory you want to keep it in. If you move it after working with it the path files will be broken

- Examine the files inside the shapefile folder. There should be .SHP, .PRJ and .DBF files

- Import the shapefile (the .shp file or the zipped folder) into QGIS using
  - the Data Source Manager toolbar, or
  - LAYER / ADD LAYER / ADD VECTOR LAYER to locate the file locally via Source selector, or
  - find the file in the Browser panel and double click to load (or drag to Layer panel)

- Add a base map: WEB / QUICK MAP SERVICES / OSM / OpenStreetMap

- The base map layer appears in the Layers panel. Just as a demonstration, reorder the layers to hide the points layer: note that the layers obscure each other. Undo these steps

- Adjust the opacity of the base map (PROPERTIES / TRANSPARENCY)

**Filter data and colour symbols**

- With a right-click on the Points layer select ‘Filter’. Select 'Grade' in Fields (upper left) then Sample or All in Values (upper right) to see what the different categories are for the ‘Grade’ variable attached to each data point. At the bottom of the dialogue box, write a SQL-like query to filter the data using a capital letter i and single quotes: Grade = 'I'

- Using the layer Properties (right-click) select the Symbology tab and adjust the colour and size of the points

- Using the Information tool on the Attributes toolbar click on a single point to see what information is attached

**Save points layer as a separate file**

- Right-click on layer, then: EXPORT / SAVE FEATURES AS. 
  - Choose FORMAT: Esri shapefile
  - Set the directory and choose a File Name

- Remove unwanted fields via: Layer RC / PROPERTIES / FIELDS / Toggle editing mode / (Select field) / Delete

**Export for web**

- WEB / QGIS2WEB / Create web map
- Under ‘Export’ tab choose a destination where it will be easy to locate the generated web files
- Under 'Appearance' select 'Show popups on hover'
<!-- - Under 'Appearance / Add Layers list', select a 'Collapsed Layers' list -->
- Option to select 'Leaflet JS'
