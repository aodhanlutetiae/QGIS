**QGIS Walkthrough 2: A points map of nuclear power stations in Europe**

**Task**
To build a map of power stations in Europe and compare different CRS

- Open a New project (PROJECT/NEW) and save it in a folder of your choice (PROJECT/SAVE AS)

- Check the CRS that the project is using as default (PROJECT/PROPERTIES/CRS): EPSG4326

- Download the shapefile of nuclear power stations from [Edinburgh Datashare](https://datashare.ed.ac.uk/handle/10283/2464?show=full).

- Import the .shp file as a vector layer into QGIS. Check the CRS under PROJECT/PROPERTIES/ INFORMATION and SOURCE: EPSG:4326. You can also check the .PRJ file in the shapefile folder.

- Add a base map: Carto darkmatter. Check (rightclick / Properties / Source) the CRS: EPSG 3857

- Download the European Countries map available at [Eurostat](https://ec.europa.eu/eurostat/web/gisco/geodata/reference-data/administrative-units-statistical-units/countries): Countries 2020 / 1 to 1 million / SHP.

- Import a European coastline and an inland layer in EPSG:3035. Hit 'cancel' for the transformation boxes.

- Compare the station in Anglesey to [Google maps](https://www.google.com/maps/place/North+Wales/@53.4141455,-4.4818501,15.89z/data=!4m5!3m4!1s0x486541b670202709:0x87f67d40aaba0eb1!8m2!3d53.0711149!4d-3.8080783)

<!-- - Right click on the base map layer (ESRI Grey Dark): LAYER CRS / SET PROJECT LAYER FROM CRS. The project and all its files are now using EPSG 3847 (WGS84 Pseudo Mercator) rather than EPSG:4326 - WGS 84

- Now compare Anglesey again in the map and in Google maps

- Resize the dots that represent the power stations -->

- Download the [global power dataset](https://datasets.wri.org/dataset/globalpowerplantdatabase) with data and latitude, longitude points

- Import into the map using the Data Source Manager (don't just drag into the Layers panel)

- Filter for just coal (solar are too numerous)

- Peg circle colour to a variable - here output power. PROPERTIES / SYMBOLOGY /  change to Graduated from the first dropdown and then change 'Method' to 'Color'. Also use Mode / Equal interval and tick 'Symmetric classification'. Finally, adjust the number ranges.
