**QGIS Walkthrough 3: Choropleth map of the Welsh Index of Multiple Deprivation**

**Task**

- To build a choropleth map of all LSOAs and of a single local authority

- Download and load [the LLE shapefile for LSOA areas in Wales](https://lle.gov.wales/catalogue/item/LowerSuperOutputAreas/?lang=en). The EPSG is OSGB1936

- Import the [wimd_19_ranking.csv](https://raw.githubusercontent.com/aodhanlutetiae/QGIS/main/wimd_19_ranking.csv) file that's in this repository. Set 'Geometry definition' to 'No geometry'. Download the [CSVT file](https://github.com/aodhanlutetiae/QGIS/raw/main/wimd_19_ranking.csvt) from this repository too - this indicates the datatype in the csv file - and place it in the same folder as your csv file

- Open the attributes table of the shapefile and the csv. Both have 1909 entries and both have a LSOA code column

- Open the properties of the shapefile and select JOINS on the left. Use + to add a new join and select the csv layer using lsoa codes: the join field is 'lsoa' from the CSV and the target field is 'LSOA' from the polygon layer

- Check the attributes table of the shapefile to see it is now carrying the data.

- Adjust the coloring to run red --> green, to reflect each LSOA's ranking (1 is most deprived, 1909 is least deprived): PROPERTIES / SYMBIOLOGY / Single Symbol --> Graduated / Value --> wimd_19_ranking_health / Color ramp / Mode --> Equal interval

- Download the shapefile for [local authority boundaries (high water mark)](http://lle.gov.wales/catalogue/item/LocalAuthorities) and import

- Filter the local authority boundaries to show just Cardiff. Use Vector / geoprocessing / clip to trim: the Input is the LSOA layer and the Overlay is the local authorities (currently filtered for just Cardiff).

- Adjust the coloring to reflect each LSOA's ranking: PROPERTIES / SYMBIOLOGY / Single Symbol --> Graduated / Value --> wimd_19_ranking_health / Color ramp / Mode --> Equal interval
