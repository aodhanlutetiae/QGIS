**QGIS Walkthrough 3: Choropleth map of the Welsh Index of Multiple Deprivation**

**Task**

- To build a choropleth map of all LSOAs and of a single local authority

**Start project & layout**

- Download and load [the shapefile for LSOA areas in Wales](https://datamap.gov.wales/layers/appdata-ons:lsoa_wales_2011). The CRS is OSGB 1936

- Download and import the [wimd_19_ranking.csv](https://github.com/aodhanlutetiae/QGIS/blob/main/wimd_19_ranking.csv) file that's in this repository ([source](https://statswales.gov.wales/Catalogue/Community-Safety-and-Social-Inclusion/Welsh-Index-of-Multiple-Deprivation)). Set 'Geometry definition' to 'No geometry'. 

- Open the attributes table of the shapefile and the csv. Both have 1909 entries and both have a LSOA code column. You can also view the attributes of an area by using the info tool (i) in the Attributes toolbar

- Open the properties of the shapefile and select JOINS on the left. Use + to add a new join and select the csv layer using lsoa codes: the join field is 'lsoa_code' from the CSV and the target field is 'LSOA11Code' from the polygon layer

- Check the attributes table of the shapefile to see it is now carrying the data, or use the i tool

- Adjust the coloring to run red --> green, to reflect each LSOA's ranking (1 is most deprived, 1909 is least deprived): PROPERTIES / SYMBOLOGY / Change from "Single Symbol" to "Graduated" / Value --> wimd_19_ranking_health / Color ramp / Mode --> Equal interval

- Project / Import-Export / Export map to image: export a .png file of your map at this stage.

===================

- Download the shapefile (high watermark) for [local authority boundaries](https://datamap.gov.wales/layergroups/inspire-wg:LocalAuthorities) and import

- Filter the *local authorities* layer to show just Cardiff. 

- Use Vector / Geoprocessing Tools / Clip: the Input is the LSOA layer and the Overlay is the local authorities (currently filtered for just Cardiff): "Only the parts of the input that fall within the Overlay layer will be added"

- Adjust the coloring - again - to reflect each LSOA's ranking: PROPERTIES / SYMBOLOGY / Single Symbol --> Graduated / Value --> wimd_19_ranking_health / Color ramp / Mode --> Equal interval

- You can remove fields that you don't want to appear, but if you edit field names the join with the CSV will break: RC / Properties / Fields / Toggle editing mode / Delete
