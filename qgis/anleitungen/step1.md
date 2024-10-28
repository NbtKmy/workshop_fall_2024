# Verschiedene Daten und Karten einlesen

## 1. Web map and data services (WM(T)S, XYZ tiles usw.) einlesen


## XYZ-Tile (slippy map tilenames)

__How to__

1. "Datenquellenverwaltung" aufmachen > "XYZ(-Verbindung)"-Symbol klicken
1. Ein Fenster taucht auf > "Neu" klicken
1. Dann taucht noch ein Fenster > Dort notwendige Information eintragen (meistens Name der Tile und URL)


__Verschiedene XYZ-Tiles__

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

## Was ist XYZ-Tile?

XYZ-Tile, auch Slippy Map Tiles genannt, stellt die Karte als Mozaik-Kacheln dar. Laut der [Erläuterung von OSM (Open Streep Map)](https://wiki.openstreetmap.org/wiki/Slippy_map_tilenames), besteht ein Teil aus 256 × 256 pixel PNG-file. 
Die ganze Kart wird durch 3 Dimensionen, X (longitude), Y (latitude) und Z (Zoom level), dargestellt. Die Kartenbilder werden nach dieser Dimension durch URL hergeholt.

Der URL der OSM-Standard-Karte sieht z.B. so aus:

```
https://tile.openstreetmap.org/zoom/x/y.png
```

Erster Teil ist Domain vom Tile-Server. Dann Zoom-Level, X und Y.

Die Erde wird durch XYZ-Tiles nach EPSG:3857 (WGS 84 / Pseudo-Mercator) als 2D-Bild dargestellt. 
D.h.: 
- Koordinaten werden nach WGS84 ([World Geodetic System 1984](https://de.wikipedia.org/wiki/World_Geodetic_System_1984)) erfasst
- Der Erdball werden nach [Pseudo-Mercator](https://en.wikipedia.org/wiki/Web_Mercator_projection) projiziert







