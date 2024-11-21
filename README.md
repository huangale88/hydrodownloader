# Climate Stations Map Application

## Overview

This application displays climate stations on interactive maps for ECCC and allows the users to interactively explore the data and download the desired information. 

## Classes & Functions

**MapLayers** creates different map layers.

**MapCreator** creates the maps centered around a specific location. In this case, Vancouver. 

**Utilities** utility functions for processing data. 
- **get_epsg_code()** Get EPSG code based on latitude and longitude.
- **create_markers()** Create markers from a DataFrame.
- **points_within_polygon()** Check if points are within a given polygon.
- **dms_to_dd()** Convert DMS (Degrees Minutes Seconds) to DD (Decimal Degrees).

**DataProcessor** Class to process climate station data.
- **process_station_data()** Process climate station data based on bounding box.

**create_app_layout()** Creates the layout of the Dash application.

**update_map_and_table()** Update the map and table based on user interactions.

   - **Parameters**:
       + **bounds (list)**: Bounds of the map view.
       + **geojson (dict)**: GeoJSON object from drawn shapes.

   - **Returns**:
       + **list**: Updated map children and table data.

## Installation

To run this application, ensure you have Python installed along with the necessary packages. You can install the required packages using pip:

```bash
pip install dash dash-leaflet pandas pyproj owslib geopandas shapely
