**Produce a map of counts by London electoral ward**

Download the ONS register of all UK geographic codes for reference: the latest version is [December 2024](https://geoportal.statistics.gov.uk/datasets/ons::register-of-geographic-codes-december-2024-for-the-uk/about). It tells us that England has 6,817 wards in use and that they all use a code that begins E05.

From the gov.uk geoportal site, download the latest (December 2022) [boundaries map](https://geoportal.statistics.gov.uk/datasets/wards-december-2022-boundaries-uk-bsc/explore) for all UK electoral wards. Download the shapefile (and the geojson if you think you might need it).

Consider the dataset. It carries two categories of crime (theft, robbery) and multiple months (March 2021 - Feb 2025) for each ward: collapse these into a single count in a pivot table. This gives 682 wards with a total of 233,461 incidents counted. A total of 19,650 incidents appear in areas with irregular area codes (-1, N/K, non-Athena) or blank area codes. Ignore for now.
Export as a CSV.

- Open QGIS and add a vector layer of the wards boundaries shapefile. Add the CSV as a text delimited layer.

- Join the two layers.

- Change the datatype on the count of incidents. PROCESSING / TOOLBOX / VECTOR TABLE / REFACTOR FIELDS ([Walkthough here](https://wiki.tuflow.com/QGIS_Change_Attribute_Type)). You'll now be using a new layer called 'Refactored'

- Assign a colour ramp: Properties / Symbology / Categorised / Value: total incidents

- Filter out (right-click) the non London areas by setting "total_incidents_wardcodes_Number of incidents" != 'NULL'

- Add a base map (Web / Quick map services / OSM) and lower its transparency (RC / Properties)

- Adjust tooltips by right-click / Properties then Display 

- Export as a webpage (Web / QGIS2Web / Create web map)
Layers & Groups: check you're exporting the Refactored layer and the base map layer (OSM Standard)
Settings: Leaflet
Export: Choose folder
Appearance: Tick Address Search, Tick Show popups on hover