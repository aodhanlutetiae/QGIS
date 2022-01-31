**QGIS Walkthrough 2: A points map of nuclear power stations in Europe**

**Task**
To build a map of power stations in Europe and compare different CRS

- Download the shapefile from [Edinburgh Datashare](https://datashare.ed.ac.uk/handle/10283/2464?show=full).

- Import the .shp file as a vector layer into QGIS. Check the CRS under PROJECT/PROPERTIES/ INFORMATION and SOURCE: EPSG:4326 - WGS84

- Download the European Countries map available at [Eurostat](https://ec.europa.eu/eurostat/web/gisco/geodata/reference-data/administrative-units-statistical-units/countries): Countries 2020 / 1 to 1 million / SHP. (A 1 to 60 million would show the effect of a larger scale with very rough coastlines)

- Import a coastline and an inland layer in EPSG:4326

- Download the the European countries base map again but the 1 to 60 million scale. Compare the layers.

- Compare the station in Anglesey to [Google maps](https://www.google.com/maps/place/North+Wales/@53.4141455,-4.4818501,15.89z/data=!4m5!3m4!1s0x486541b670202709:0x87f67d40aaba0eb1!8m2!3d53.0711149!4d-3.8080783)

- Right click on the base map layer (ESRI Grey Dark): LAYER CRS / SET PROJECT LAYER FROM CRS. The project and all its files are now using EPSG 3847 (WGS84 Pseudo Mercator) rather than EPSG:4326 - WGS 84

- Now compare Anglesey again in the map and in Google maps

- Resize the dots that represent the power stations

- Download the [global power dataset](https://datasets.wri.org/dataset/globalpowerplantdatabase) with data and latitude, longitude points

- Import into the map

- Filter for just coal (solar are too numerous)

- Peg circle colour to a variable - here output power. SO: "For anyone who is coming to this question and finds the links provided dead, you can achieve this by going into layer properties -> Symbology -> change to Graduated from the first dropdown and then change 'Method' to 'Size'."" | Also use Mode / Equal interval

**CUT**
- Add a base map (WEB/QUICK MAP SERVICES): ESRI grey (dark). Check the CRS (via right click / Properties): EPSG 3857 WGS84 Pseudo Mercator
