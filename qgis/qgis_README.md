# QGIS





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

https://gisgeography.com/free-global-dem-data-sources/

https://srtm.csi.cgiar.org/srtmdata/

https://docs.qgis.org/2.18/en/docs/training_manual/foreword/preparing_data.html

https://www.jawfish-paradise.com/line_point_polygon/

https://www.mierune.co.jp/blog/posts/x0181eghaj84?lang=ja
