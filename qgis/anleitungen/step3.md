# Verschiedene Daten und Karten einlesen

## Vektordaten behandeln

Wir haben bereits eine Linie beim Step2 erstellt. Dies ist eine Vektordaten. 
Vektordaten bestehen, einfach gesagt, aus Punkte und Linien. Die Elemente von Vektordaten sind Punkte, Linie und Poligon (Fläche, die durch Linie umgeschlossen sind).

## Wo findet man Vektordaten?

Es sind viele Vektordaten im Internet zu finden! Hier 2 Beispiele:

### Overture Maps (Overture Maps Foundation)

Founded in 2022 under the Joint Development Foundation, Overture is dedicated to the development of reliable, easy-to-use, and interoperable open map data that will power current and next-generation map products. We build this data through a collaborative process that combines technology, data, and support from a wide range of companies.

Members: Amazon, Meta, Microsoft usw...

Man kann folgende Datentypen herunterladen: address|building|building_part|division|division_area|division_boundary|place|segment|connector|infrastructure|land|land_cover|land_use|water

Die Daten kann man z.B. durch python geholt werden. ([Beispiel](https://colab.research.google.com/drive/1yjS37YgWVqVXvzZFJ8XLmUmCbOeQygFA?usp=sharing))

Laut der [Anleitung](https://docs.overturemaps.org/getting-data/overturemaps-py/) durch Python kann man Vector-Daten holen.

```
$ pip install overturemaps
$ overturemaps download --bbox=8.528265,47.364406,8.558316,47.384746 \
    -f geoparquet --type=building --output=zurich.geoparquet
```

Den Wert vom Parameter "bbox" kann man von "[Boundingbox von Klokantech](https://boundingbox.klokantech.com/)" holen. 

1. Einfach den Bereich auswählen 
1. Unten bei "Copy&Paste" (Format "CSV") anwählen und Kopieren

Unter dem Ordner "data" sind verschiedene "Geoparquet"-Daten zu finden. Heute wollen wir 2 Daten "zurich_buildings.geoparquet" und "zurich_segment.geopartquet" anzeigen. 
1. Zuerst sie herunterladen
1. Durch Drag&Drop die Daten in QGIS einbeziehen.  Fertig!



### GeoBoundaries

William & Mary geoLab bietet ein Plattform an, woher man die Vektordaten von Verwaltungsgrenze herunterladen kann.

Dies ist der URL zur Plattform:

https://www.geoboundaries.org/countryDownloads.html

Heute verwenden wir die Datei "geoBoundaries-CHE-ADM1.geojson". 
1. Hier auch zuerst herunterladen
1. Und Drag&Drop! Fertig


