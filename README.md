## Jupyter Notebooks for urban studies

**Jupyter Notebooks working with Yandex and HERE API to ease urban planning process.**

1. [Geocoding notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/geocoding_api.ipynb) works with [Yandex Geocoding API](https://tech.yandex.ru/maps/geocoder/doc/desc/concepts/about-docpage/), it allows you to retrieve coordinates in response to given address in pandas dataframes. Free limit with API key is 25K requests per day

2. [Organization search notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/yandex_organization_api.ipynb) works with [Yandex Organization search](https://tech.yandex.ru/maps/geosearch/doc/concepts/request-docpage/), retrieving organization points with coordinates according to given list of types within bounding box. Free limit with API key is 500 requests per day, 500 organizations in each request

3. [Isolines notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/isohrones_api.ipynb) works with [HERE isoline API](https://developer.here.com/documentation/routing/dev_guide/topics/resource-calculate-isoline.html), returning polygons of isolines for given list of points in two formats - WKT and one suitable for `folium`, free limit with API key is 250K requests per month

4. [Overpass notebook](https://github.com/skaryaeva/urban_studies_notebooks/blob/master/osm_python_tools.ipynb) using [OSMPythonTools library](https://github.com/mocnik-science/osm-python-tools), retrieves OSM POI with coordinates according to given list of types within bounding box

All the data examples used for notebooks are contained in `input_params.xlsx`, example for API keys storage is in `api_keys_example.xlsx`


Libraries used:
- `pandas`
- `requests`
- `folium`


## Issues list
- timeout problem with overpass api