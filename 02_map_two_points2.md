**QGIS Walkthrough 2: A points map of power stations**

**Task**

- Build a map of power stations (2011)

**Start project & layout**

- Open a New Project (PROJECT / NEW) and save it in a location of your choice (PROJECT / SAVE AS)

- Download the shapefile of nuclear power stations from [Edinburgh Datashare](https://datashare.ed.ac.uk/handle/10283/2464?show=full) ('Download all files')

- Import the .shp file or zipped SHP folder as a vector layer into QGIS. Check the CRS under PROJECT / PROPERTIES / INFORMATION and SOURCE: EPSG:4326. (You can also check the .PRJ file in the shapefile folder)

- Download the Countries map available at [Eurostat](https://ec.europa.eu/eurostat/web/gisco/geodata/reference-data/administrative-units-statistical-units/countries) on a 1 to 1 million scale: Countries 2020 / 1 to 1 million / SHP

- Import a coastline and an inland layer (in EPSG:4326)
	CNTR_BN_01M_2020_4326_COASTL.shp.zip
	CNTR_BN_01M_2020_4326_INLAND.shp.zip	

- Add a base map 

- Download the [global power CSV dataset](https://datasets.wri.org/dataset/globalpowerplantdatabase) that holds data including latitude / longitude points

- Import the CSV into the map using the Data Source Manager, choosing 'Delimited text' in the left panel options and ensuring 'Geometry definition' has 'Point coordinates' and that there is a CRS selected. (Or Layer / Add Layer / Add delimited text layer)

- Filter for just coal-powered stations using RC / FILTER / Fields / Primary fuel

	- Link circle colour for the power stations to a variable - output power. PROPERTIES / SYMBOLOGY /  change the first dropdown (at the top) from 'Single Symbol' to 'Graduated'. Select 'capacity_mw' under Value. Change 'Method' to 'Color'. 

	- At the bottom, use Mode / Equal interval (Tick / untick 'Symmetric classification' to get the categories to show, if necessary). Adjust the number of classes to 7, or another number if it works better. Finally, adjust the number ranges.
