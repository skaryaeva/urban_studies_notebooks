## Jupyter Notebooks for urban studies

**Jupyter Notebooks working with Yandex and HERE API to ease urban planning process.**

***Geocoding***

1. [Yandex geocoding notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/geocoding_yandex_api.ipynb) works with [Yandex Geocoding API](https://tech.yandex.ru/maps/geocoder/doc/desc/concepts/about-docpage/), returning a shp file as a result. Free limit for HTTP GET request is now only 1000 addresses per day. [Open data about housing](https://www.reformagkh.ru/opendata?gid=2353101&cids=house_management&page=1&pageSize=10) is used for the example.

2. [HERE geocoding notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/geocoding_here_api.ipynb) works with [HERE Geocoding and Search API](https://developer.here.com/documentation/geocoding-search-api/api-reference-swagger.html), free limit is 250k requests per month. [Open data about housing](https://www.reformagkh.ru/opendata?gid=2353101&cids=house_management&page=1&pageSize=10) is used for the example

***Drawing a grid and calculating population density***

3. [Draw a grid](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/grid_population_density.ipynb) with a designated cell size based on city OSM name, delete all the cells outside of administrative borders and completely in the water, saving the result in `shp`, add population data based on geocoded housing in notebook 2.

***Organization search***

4. [Yandex organization search notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/yandex_organization_api.ipynb) works with [Yandex Organization search](https://tech.yandex.ru/maps/geosearch/doc/concepts/request-docpage/), retrieving organization points with coordinates according to given list of types within bounding box. Free limit with API key is 500 requests per day, 500 organizations in each request

5. [HERE places search notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/here_places_search.ipynb) works with [HERE Places (Search) API](https://developer.here.com/documentation/places/dev_guide/topics_api/resource-explore.html), which is in maintenance now. The grid created in notebook 3 is used for retrieving the data.

6. [Overpass notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/osm_python_tools.ipynb) using [OSMPythonTools library](https://github.com/mocnik-science/osm-python-tools), retrieves OSM POI with coordinates according to given list of types within bounding box

***Isolines***

7. [Isolines notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/isohrones_api.ipynb) works with [HERE isoline API](https://developer.here.com/documentation/routing/dev_guide/topics/resource-calculate-isoline.html), returning polygons of isolines for given list of points in WKT format used for geodataframes, free limit with API key is 250K requests per month.

8. [Public transport isohrones notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/public_transport_api.ipynb) works with [HERE public transport API](https://developer.here.com/documentation/transit/dev_guide/topics/resource-isochrone-search.html), receiving list of stations with coordinates and minutes spent to reach it, and then goes to [HERE isoline API](https://developer.here.com/documentation/routing/dev_guide/topics/resource-calculate-isoline.html) for calculating pedestrian isolines for the rest of given time, thus drawing a public transport isohrone.





Main libraries used:
- `pandas`
- `geopandas`
- `requests`
- `folium`


## Issues list
- timeout problem with overpass api