# QGIS



## XYZ-Tiles


### Open Streep Map

https://tile.openstreetmap.org/{z}/{x}/{y}.png

Sonst siehe auch Wiki von OSM
https://wiki.openstreetmap.org/wiki/Raster_tile_providers

### Swisstopo

https://api3.geo.admin.ch/services/sdiservices.html#xyz
... Also z.B. https://wmts.geo.admin.ch/1.0.0/ch.swisstopo.swissimage/default/current/3857/{z}/{x}/{y}.jpeg


### Google

__Google Hybrid__
https://mt1.google.com/vt/lyrs=y&x={x}&y={y}&z={z}

__Google Satellit__
https://mt1.google.com/vt/lyrs=s&x={x}&y={y}&z={z}

__Bing Luftbild__
http://ecn.t3.tiles.virtualearth.net/tiles/a{q}.jpeg?g=1



## Vector Daten

### Overture Maps

Laut der [Anleitung](https://docs.overturemaps.org/getting-data/overturemaps-py/) durch Python kann man Vector-Daten holen.

```
$ pip install overturemaps
$ overturemaps download --bbox=8.528265,47.364406,8.558316,47.384746 \
    -f geoparquet --type=building --output=zurich.geoparquet

```
Den Wert vom Parameter "bbox" kann man von "[Boundingbox von Klokantech](https://boundingbox.klokantech.com/)" holen. 

1. Einfach den Bereich auswählen 
1. Unten bei "Copy&Paste" (Format "CSV") anwählen und Kopieren

### GeoBoundaries

https://www.geoboundaries.org/countryDownloads.html