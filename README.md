# Leaflet and ArcGIS location services
_Plenary demo for day one of the Esri Dev Summit 2022, Patrick Arlt and Anita Kemp_ 

You can easily integrate ArcGIS location services with your application built with an open source mapping API. To learn more, you can visit: 
  - [Esri Leaflet](https://developers.arcgis.com/esri-leaflet/) 
  - [OpenLayers and ArcGIS location services](https://developers.arcgis.com/openlayers/)
  - [Mapbox GL JS/Map Libre and ArcGIS location services](https://developers.arcgis.com/mapbox-gl-js/) 

You can view the live demo [here](http://os-dev-summit-2022.surge.sh/). 

## Demo app context 

A real estate company has built an application using Leaflet that displays locations of properties in an area. However, the app can be improved using the Esri Leaflet plugin and ArcGIS location services. These updates include: 

  * Switching out the basemap layer 
  * Accessing data from a hosted feature service
  * Returning relevant demographic data from the GeoEnrichment service

### Demo 1 

This is the original application. It uses the OpenStreetMap basemap layer and displays some properties on the map fetched from the `listings.csv` file. When you click on a point, you will see the building:

  * type
  * rate
  * size

### Demo 2

This demo switches out the OSM basemap layer to use an ArcGIS basemap layer, in this case `ArcGIS:Community`. To learn more about the available basemap enumerations, visit the [Basemap layer service](https://developers.arcgis.com/documentation/mapping-apis-and-services/maps/services/basemap-layer-service/#basemapstyle) page in the _Mapping APIs and location services_ guide. 

### Demo 3

The next demo addresses the data. Instead of using `fetch`, it uses Esri Leaflet's `featureLayer` class to access the data from a hosted feature serivce. To learn more, visit [Feature service](https://developers.arcgis.com/documentation/mapping-apis-and-services/data-hosting/services/feature-service/) in the _Mapping APIs and location services_ guide. 

### Demo 4

The last demo returns demographic data from the GeoEnrichment service. The data include: retail spending, restaurant spending, and general income/population information. To learn more, visit the [GeoEnrichment service](https://developers.arcgis.com/documentation/mapping-apis-and-services/demographics/services/geoenrichment-service/) page in the _Mapping APIs and location services_ guide. 

## Prequisites to run the code

You will need an ArcGIS account, an API key, and a feature layer created from the `listings.csv` data. 

1. If you don't have an account, you can sign up [here](https://developers.arcgis.com/sign-up/) for a free developer account. 
2. In your **Dashboard**, find your API key. Be sure to configure your key to access the services. 
3. To use the `featureLayer` class in demos 3-4, you will need to import the CSV data to create a feature layer. To learn more, visit the [Import data as a feature layer](https://developers.arcgis.com/documentation/mapping-apis-and-services/data-hosting/tutorials/tools/import-data-as-a-feature-layer/) tutorial. 

NOTE: Your feature layer can be accessed either publically or privately. If you want to keep your layer private, scope your API key to access the item. 

## Run the code

1. Clone this repository 
2. Replace "YOUR_API_KEY" with an API key that is scoped to access the basemap layer service, the GeoEnrichment service, and (optionally) your hosted feature layer. 
3. In **Demos 3 and 4**, replace "SERVICE_URL" with your feature layer's service URL. 
4. Type `npm install` to install dependencies 
5. Type `npm start` to run the code locally. 

You will see a page with links to four demos. **To see it live, click [here](http://os-dev-summit-2022.surge.sh/)**. 

## License and copyright 

Copyright 2022 Esri 

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
