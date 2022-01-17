<font size="4">
QGIS Walkthrough 2: A points map of nuclear power stations in Europe
</font>

- Download the shapefile from [Edinburgh Datashare](https://datashare.ed.ac.uk/handle/10283/2464?show=full).

- Examine the .prj file:
GEOGCS["GCS_WGS_1984",DATUM["D_WGS_1984",SPHEROID["WGS_1984",6378137.0,298.257223563]],PRIMEM["Greenwich",0.0],UNIT["Degree",0.0174532925199433]]

- Import the .shp file as a vector layer into QGIS. Check the CRS under Properties / Information and Properties / Source: EPSG:4326 - WGS 84

- Add two base maps (WEB / QUICK MAP SERVICES): ESRI grey (dark) and Carto Dark Matter

- Check (via Properties) the CRS. All are EPSG 3857 (WGS84 Pseudo Mercator)

- Add the European Countries map available at Eurostat. (Countries 2020 / 1 to 1 million / SHP)> EPSG:3035 - ETRS89-extended / LAEA Europe

You now have geodata that came in three forms:
- nuclear power stations    
  - EPSG:4326 - WGS 84
- ESRI grey (dark) base map  
  - EPSG 3847 (WGS84 Pseudo Mercator)
- Europe countries        
  - EPSG:3035 - ETRS89-extended / LAEA Europe

ESRI [writes](https://www.esri.com/arcgis-blog/products/arcgis-solutions/defense/what-does-the-nga-web-mercator-advisory-mean-for-esri-defense-and-intelligence-users/): *Web Mercator, called “WGS 1984 Web Mercator (auxiliary sphere)” in ArcGIS, and also known as “EPSG: 3857” (European Petroleum Survey Group) and “WGS 84/Popular Visualisation Pseudo-Mercator”, was popularized by Google and has become the most commonly-used coordinate system for web mapping applications. It is currently used by Google Maps, Bing Maps, and Esri ArcGIS Online basemaps, among others.*

- Download the the European countries base map again but the 1 to 60 million scale. Compare the layers.

- Compare the station in Anglesey to [Google maps](https://www.google.com/maps/place/North+Wales/@53.4141455,-4.4818501,15.89z/data=!4m5!3m4!1s0x486541b670202709:0x87f67d40aaba0eb1!8m2!3d53.0711149!4d-3.8080783)

- Right click on the base map layer (ESRI Grey Dark): LAYER CRS / SET PROJECT LAYER FROM CRS. The project and all its files are now using EPSG 3847 (WGS84 Pseudo Mercator) rather than EPSG:4326 - WGS 84

- Now compare Anglesey again in the map and in Google maps

- Resize the dots that represent the power stations
