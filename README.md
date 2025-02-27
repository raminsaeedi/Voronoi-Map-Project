# Voronoi Map Generator

A Python tool that creates Voronoi region maps based on location data, supporting both shapefile and GeoJSON/TopoJSON input formats.

## Example Output

![Example/voronoi_regions.png](https://github.com/raminsaeedi/Voronoi-Map-Project/blob/main/Example/voronoi_regions.png)

#### The tool generates professional visualizations where:The tool generates professional visualizations where:

- Each business unit is represented with a distinct color
- City points are clearly marked
- Region boundaries are precisely defined
- Areas are calculated in square kilometers

## 🌟 Features

#### - Business Unit Visualization

Color-coded regions by business unit with customizable transparency
Clear boundaries between territories
City location markers with labels

#### - Flexible Map Input Support

Shapefiles (in ZIP format)
GeoJSON files
TopoJSON files

#### - Intelligent Point Management

Automatic filtering of points outside map boundaries
Visual distinction between included and excluded locations

#### - Professional Output Formats

High-resolution PNG maps (300 DPI)
Styled GeoJSON with proper attributes for geojson.io
Detailed area calculations per region

## 📋 Requirements

- Python 3.6+
- GeoPandas
- Matplotlib
- Shapely
- GeoVoronoi
- NumPy
- Pandas

## 🔧 Installation

```python
# Install with plotting dependencies (recommended):
pip install geovoronoi[plotting]

# Alternative installation with explicit dependencies:
pip install geovoronoi descartes requests
```

## 📚 Imports

```python
import logging
from pprint import pprint
import matplotlib.pyplot as plt
import numpy as np
import geopandas as gpd
from shapely.geometry import Polygon, Point, MultiPolygon
import requests
import tempfile
import os
import pandas as pd
import zipfile
import json
import matplotlib.colors as mcolors
from geovoronoi import coords_to_points, points_to_coords, voronoi_regions_from_coords, calculate_polygon_areas
from google.colab import files
```

## 🚀 Usage

This tool was designed to run in Google Colab but can be adapted for local use.

1. Upload your CSV file with location data (must contain columns for City, Business_Unit, Latitude, and Longitude)
2. Upload your map file (either a ZIP containing a shapefile or a GeoJSON/TopoJSON file)
3. The script will generate:
   - A visualization of the Voronoi regions
   - A GeoJSON file for use with geojson.io
   - A mapping of regions to cities with area calculations

## License

[MIT License](LICENSE)
