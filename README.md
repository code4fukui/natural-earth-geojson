# Natural Earth data in GeoJSON

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

[Natural Earth](http://www.naturalearthdata.com) is a public domain map dataset available at 1:10m, 1:50m, and 1:110 million scales. The original vector data is provided as [ESRI shapefiles](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf). This repository provides the same data converted to [GeoJSON](http://geojson.org) for easy use in web mapping and other applications.

Each GeoJSON file is also provided in a compressed 7-Zip archive (`.7z`) to reduce file size.

<img src="logo.png" alt="Natural Earth GeoJSON Logo">

## Usage

You can use this data by either cloning the repository or downloading individual files directly from the folders. The data is organized by scale and theme:

-   `10m/` (1:10,000,000)
-   `50m/` (1:50,000,000)
-   `110m/` (1:110,000,000)

Within each scale directory, the data is further divided into `cultural/` and `physical/` themes.

## Data Themes

The following tables, adapted from the [Natural Earth features page](http://www.naturalearthdata.com/features), provide an overview of the available data.

### Cultural

| Theme | Description | 1:10m | 1:50m | 1:110m |
| :--- | :--- | :---: | :---: | :---: |
| **Countries** | Boundary lines and polygons for countries and sovereign states, including dependencies. | Yes | Yes | Yes |
| **Disputed areas** | Polygons for disputed areas and breakaway regions, from Kashmir to Western Sahara. | Yes | Yes | |
| **First order admin** | Internal boundaries for provinces, departments, states, etc. | Yes | Yes | |
| **Populated places** | Point symbols with name attributes for capitals, major cities, and other significant towns. | Yes | Yes | Yes |
| **Urban polygons** | Urban area polygons derived from 2002-2003 MODIS satellite data. | Yes | Yes | |
| **Parks & protected areas** | U.S. National Park Service units. | Yes | | |
| **Pacific nation groupings** | Bounding boxes for organizing Pacific island nations. | Yes | Yes | Yes |
| **Water boundary indicators** | A selection of 200-mile nautical limits, disputed lines, and treaty lines. | Yes | | |

### Physical

| Theme | Description | 1:10m | 1:50m | 1:110m |
| :--- | :--- | :---: | :---: | :---: |
| **Coastline** | Ocean coastline, including major islands, matched to land and water polygons. | Yes | Yes | Yes |
| **Land** | Land polygons, including major islands. | Yes | Yes | Yes |
| **Ocean** | Ocean polygons split into contiguous pieces. | Yes | Yes | Yes |
| **Minor Islands** | Small ocean islands ranked by relative importance. | Yes | | |
| **Reefs** | Major coral reefs. | Yes | | |
| **Physical region features** | Polygon and point labels for major physical features. | Yes | Yes | Yes |
| **Rivers & Lake Centerlines** | Ranked by relative importance, with name and line width attributes. | Yes | Yes | Yes |
| **Lakes** | Ranked by relative importance, coordinating with river ranking. | Yes | Yes | Yes |
| **Glaciated areas** | Polygons for glaciers, including name attributes for major polar glaciers. | Yes | Yes | Yes |
| **Antarctic ice shelves** | Reflects recent ice shelf collapses. | Yes | Yes | |
| **Bathymetry** | Nested polygons for depths from 0 to -10,000 meters. | Yes | | |
| **Geographic lines** | Polar circles, tropics, equator, and the International Date Line. | Yes | Yes | Yes |
| **Graticules** | Latitude and longitude lines in 1, 5, 10, 15, 20, and 30-degree increments. | Yes | Yes | Yes |

## Conversion Process

The conversion from shapefile to GeoJSON is performed using [ogr2ogr](http://www.gdal.org/ogr2ogr.html), a command-line utility from the [Geospatial Data Abstraction Library](http://www.gdal.org) (GDAL). You can find installation instructions and binaries on the GDAL website. For Debian-based systems, it is available in the `gdal-bin` package.

## Data Version

The data in this repository is based on Natural Earth [version 4.0.0](http://www.naturalearthdata.com/updates/mail.cgi?flavor=archive;list=updates;id=20171103122417), released on November 3, 2017.

## Disclaimer

Per the Natural Earth [disclaimer regarding disputed areas](http://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-0-countries/):

> Natural Earth Vector draws boundaries of countries according to de facto status. We show who actually controls the situation on the ground. Please feel free to mashup our disputed area themes to match your particular political outlook.
