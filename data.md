### Data sources
Three sources of data are considered to address the business problem: Foursquare Places API, Chicago GEO json, Chicago Demographics Data, and List of neighborhoods in Chicago:
* [Chicago GEO json](https://raw.githubusercontent.com/seattleio/seattle-boundaries-data/master/data/neighborhoods.geojson) - Defines geospatial shape (boundaries) of Chicago neighborhoods. This geo json file will be used for area calculation and visualization purposes.
* [Foursquare Places API](https://developer.foursquare.com/docs/api) - API that helps to get venues at the specific location. Although there are some limitations of API access, this source is considered as a main provider of most up-to-date venues data.  
* [Chicago Demographic Data](https://datahub.cmap.illinois.gov/dataset/community-data-snapshots-raw-data) - Chicago demographic, income, and education data by community in CSV format and corresponding columns description file. Might be inaccessible out of USA.
* [OpenCage Geocoder](https://opencagedata.com/api) - API that will be used reverse geocoding, e.g. to get address by geospatial data. 

### Considered impact factors by data source
The following table describes data source for the considered impact factors.
  
| factor | data item | data source |
|---|---|---|
| Demographics of the neighborhood | communities boundaries | Chicago GEO json | 
| Demographics of the neighborhood | population, population density | Chicago Demographics Data |
| Demographics of the neighborhood | income, education, employment status, industries, occupation, sex and age | Chicago Demographics Data |
| Facility Accessibility | nearby parkings, transport stops | Foursquare Places API |
| Competitors | nearby gym facilities, rating | Foursquare Places API |
| Adjacent Tenants | "conflicting" venues | Foursquare Places API |
| Adjacent Tenants | relevant (supportive) venues | Foursquare Places API |
| Adjacent Tenants | reverse geocoding | OpenCage Geocoder |