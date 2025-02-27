# Voronoi Map Generator

A Python tool that creates Voronoi region maps based on location data, supporting both shapefile and GeoJSON/TopoJSON input formats.

## Features

- Generate Voronoi regions colored by business unit
- Support for multiple input map formats:
  - Shapefiles (in ZIP format)
  - GeoJSON files
  - TopoJSON files
- Automatic point filtering to ensure all points lie within map boundaries
- Export to GeoJSON with proper styling for visualization in geojson.io
- High-quality PNG output with custom styling

## Requirements

- Python 3.6+
- GeoPandas
- Matplotlib
- Shapely
- GeoVoronoi
- NumPy
- Pandas

## Usage

This tool was designed to run in Google Colab but can be adapted for local use.

1. Upload your CSV file with location data (must contain columns for City, Business_Unit, Latitude, and Longitude)
2. Upload your map file (either a ZIP containing a shapefile or a GeoJSON/TopoJSON file)
3. The script will generate:
   - A visualization of the Voronoi regions
   - A GeoJSON file for use with geojson.io
   - A mapping of regions to cities with area calculations

## Example Output

![Example/voronoi_regions.png](https://github.com/raminsaeedi/Voronoi-Map-Project/blob/main/Example/voronoi_regions.png)

## License

[MIT License](LICENSE)
