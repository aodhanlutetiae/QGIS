**QGIS Walkthrough 2: A points map of power stations**

**Task**

- Build a map of power stations

**Start project & layout**

- Open a New Project (PROJECT / NEW) and save it in a location of your choice (PROJECT / SAVE AS)

- Under WEB / QUICK MAP SERVICES add a base map layer

- Download the shapefile of 2011 global nuclear power stations from [Edinburgh Datashare](https://datashare.ed.ac.uk/handle/10283/2464?show=full) ('Download all files'). Upzip the download to get to the zipped shapefile folder.

- Import the .shp file or zipped SHP folder as a vector layer into QGIS. Check the CRS under PROJECT / PROPERTIES / INFORMATION and SOURCE: EPSG:4326. (You can also check the .PRJ file in the shapefile folder)

- Download the [global power CSV dataset](https://datasets.wri.org/dataset/globalpowerplantdatabase) that holds data including latitude / longitude points. Use version 1.3 from 2021

- Import the CSV into the map using the Data Source Manager, choosing 'Delimited text' in the left panel options and ensuring 'Geometry definition' has 'Point coordinates' and that there is a CRS selected. (Or Layer / Add Layer / Add delimited text layer)

- Filter for just coal-powered stations using RC / FILTER / Fields / Primary fuel

	- Link circle colour for the power stations to a variable - output power. PROPERTIES / SYMBOLOGY /  change the first dropdown (at the top) from 'Single Symbol' to 'Graduated'. Select 'capacity_mw' under Value. Change 'Method' to 'Color'. 

	- At the bottom, use Mode / Equal interval (Tick / untick 'Symmetric classification' to get the categories to show, if necessary). Adjust the number of classes to 7, or another number if it works better. Finally, adjust the number ranges.
