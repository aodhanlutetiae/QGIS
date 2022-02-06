**QGIS Walkthrough 2: A points map of nuclear power stations in Europe**

**Task**
- Build a map of power stations in Europe

- Open a New Project (PROJECT / NEW) and save it in a location of your choice (PROJECT / SAVE AS)

- Check the CRS that the project is using as default (PROJECT / PROPERTIES / CRS)

- Download the shapefile of nuclear power stations from [Edinburgh Datashare](https://datashare.ed.ac.uk/handle/10283/2464?show=full)

- Import the .shp file as a vector layer into QGIS. Check the CRS under PROJECT / PROPERTIES / INFORMATION and SOURCE: EPSG:4326. You can also check the .PRJ file in the shapefile folder

- Download the European Countries map available at [Eurostat](https://ec.europa.eu/eurostat/web/gisco/geodata/reference-data/administrative-units-statistical-units/countries): Countries 2020 / 1 to 1 million / SHP

- Import a European coastline and an inland layer in EPSG:4326

- Add a base map: Carto darkmatter. Check (rightclick / Properties / Source) the CRS: EPSG:3857

- Download the [global power dataset](https://datasets.wri.org/dataset/globalpowerplantdatabase) that holds data including latitude / longitude points

- Import the CSV into the map using the Data Source Manager (don't just drag into the Layers panel), choosing 'Geometry definition' as 'Point coordinates' (and with EPSG:4326 selected)

- Filter for just coal-powered stations using RC / FILTER / Fields / Primary fuel

- Link circle colour for the power stations to a variable - output power. PROPERTIES / SYMBOLOGY /  change the first dropdown from 'Single Symbol' to 'Graduated'. Select 'Capacity' under Value. Change 'Method' to 'Color'. Also use Mode / Equal interval and tick / untick 'Symmetric classification' to get the categories to show. Adjust the number of classes to 7. Finally, adjust the number ranges
