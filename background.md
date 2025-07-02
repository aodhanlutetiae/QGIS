**Background**

Quantum GIS 1.0 was released in 2009; when version 2.0 was released in 2013, the name was changed to QGIS. Room 1.03 (JOMEC) will install 3.30 and 3.22 is a good alternative.

GIS:    Geographic Information System

Shapefile:  A folder of files with the same name but different filetype extensions that includes geographical coordinates like points or lines (.shp) and a database of associated information (.dbf), as well as some optional files such as projections (.prj).

WGS 84: The World Geodetic System 1984 (WGS 84). A 3-dimensional coordinate reference system for establishing latitude, longitude and heights.

**[EPSG (European Petroleum Survey Group) codes](https://epsg.io)**

- EPSG 4326   WGS 1984
  - Esri [writes](https://developers.arcgis.com/documentation/spatial-references/): 4326 is the most common spatial reference for storing a referencing data across the entire world. It serves as the default for both the PostGIS spatial database and the GeoJSON standard

- EPSG 3857   WGS 1984 / Pseudo Mercator
  - ESRI [writes](https://www.esri.com/arcgis-blog/products/arcgis-solutions/defense/what-does-the-nga-web-mercator-advisory-mean-for-esri-defense-and-intelligence-users): Web Mercator [...] was popularized by Google and has become the most commonly-used coordinate system for web mapping applications. 

- EPSG 27700  OSGB1936
  - British National Grid, UK Ordnance Survey

- EPSG 3035   ETRS89-extended
  - Used for mapping Europe

DEM:    Digital elevation model. A 3d representation of terrain using raster (not vector) files that use a grid of pixels.
