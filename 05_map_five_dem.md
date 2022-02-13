**QGIS Outline 5: An elevation map with DEM raster files**

- Download and import (as a raster file) a [DEM file for Wales](https://ec.europa.eu/eurostat/web/gisco/geodata/reference-data/elevation/copernicus-dem/elevation). The file is 137MB in size. Rename it

- Centre the map on Caerphilly mountain *with longitude, latitude* (-3.2250799644385144, 51.562159129179356) using the coordinate box in the bottom left, then adjust to reach the coast

- RASTER / EXTRACTION / CLIP RASTER BY EXTENT / Clipping extent --> Use Map Canvas Extent

- RASTER / EXTRACTION / CONTOUR / Ensure the input layer is the clipped raster not the entire original file / Interval between contour lines --> 10m

- Adjust the Properties / Symbology for the contour layer: Graduated / Value = Elevation

- Adjust the Properties / Symbology for the cropped raster layer: Transparency (20%) / Render band --> Single band pseudo colour / Mode --> Equal Interval / 4 categories at 0, 1, 250, 500 with the first one in blue and the others in green
