# Verschiedene Daten und Karten einlesen

## 2. Rasterdaten einlesen

__How to__

1. Aus diesem Github-Repo `/qgis/data/swiss_dem_example.tif`herunterladen und irgendwo lokal speichern
1. "Datenquellenverwaltung" in QGIS klicken > "Raster" auswählen
1. Im Popup-Fenster "Queltyp" = Datei und "Quelle" = Pfad zu der geoTIFF-Datei eingeben
1. "Hinzufügen" klicken - dann sollte das Bild in QGIS erscheinen
1. Falls Koordinatenbezugssysteme (KBS) anderes als EPSG:3857 ist, dann ändern...

Ein wenig farbiger machen...
1. Layer (linke Spalte unten) mit Maus-Rechts klicken
1. "Eigenschaft" klicken > Im Popup-Fenster "Symbolisierung" klicken > Darstellungsart zu "Paletten- /Endeutige Werte" ändern > Einen Farbverlauf auswählen \
    dann "Klassifizieren" klicken > "Anwenden" klicken
1. Man kann auch Transparanz der Layer bei "Transparenz" steuern...



## Was ist Rasterdaten?

Rasterdaten ist ... einfach gesagt digitales Bild mit Geodaten. Die Pixels in einer GeoTiff-File haben zusätzlcih spezielle Daten über die Georeferenz (Koordinaten und ggf. Höhendaten). In unseren Beispiele verwenden wir sogenannte DEM-Daten in GeoTIFF-format.

### DEM (digital elevation model)?

... bitte diesen Wikipedia-Aritkel [Digitales Höhenmodell](https://de.wikipedia.org/wiki/Digitales_H%C3%B6henmodell) anschauen.
Wir verwenden hier SRTM(Shuttle Radar Topography Mission)-Daten, die digitale Geländermodell darstellen soll.

![](https://upload.wikimedia.org/wikipedia/commons/2/24/DOM_DGM.png)

(Quelle: Wikimedia Commons)



## Eine Funktion von QGIS ausprobieren!
__Geländehöhenprofil__ ist eine Funktion, die seit 2022 (Version 3.26) in QGIS eingeführt worden ist. Mit dieser Funktion kann man ganz schnell die Geländehöhenprofil erstellen!

1. Nachdem eine DEM-Layer eingespielt ist, klickt man "Ansicht" in der Menüwerkzeugleiste.
1. "Geländehöhenprofil klicken > dann taucht ein weiteres Fenster unten auf. Dort sollte die DEM-Layer schon eingezeigt sein
1. In dem unterem Fenster klickt man das Symbol "Kurve Aufnehmen". Danach den Maus-Kursor auf die Karte führen. Der Maus-Pointer sieht jetzt anders aus
1. Nun kann man jetzt mit Maus-Links-Klick die Punkte für die Linie setzen, für die Geländehöhenprofil gemacht werden sollte. Man kann mehrere Punkte setzen.
1. Wenn man die Linie stoppen will, Maus-Rechts-Klick... Dann wird schon die Profil erstellt 

## ... Okay, wie verwende ich aber das Ergebnis?

Man könnte folgendermassen verfahren:
1. Zuerst eine neue Vektorlayer für eine Linie erstellen
    1. "Neuer Shapedateilayer erstellen" klicken
    1. Dateiname und Speicherort bestimmen
    1. Geometrietyp "Linie" auswählen
    1. Ggf. Koordinatensystem anpassen 
    1. "OK" - Danach wird eine Layer erstellt
    1. Dann die Layer in der linken Spalte aktivieren (einmal klicken, dann wird's blau markiert). Danach das "Bleistift"-Symbol klicken. So wird der Bearbeitungsmodus eingeschaltet. 
    1. Dann "Linienobjekt hinzufügen" klicken - und so wie vorher die Linie ziehen (mit Maus-Links-Klick Punkte setzen, mit Maus-Rechts-Klick Linie-Ziehen beenden)
    1. Ein Popup-Fenster kommt auf und fragt nach ID-Nummer. Einfach beliebige ID schreiben. Speichern.
    1. Die Linie ist da, aber wahrscheinlich unsichtbar. Durch "Eigenschaft" die Liniendarstellung ändern.
1. Dann das Symbol "Neues Drucklayout" klicken
1. Ins Drucklayout alle gewünschte Elemente importieren und ggf. Beschriftungen noch hinzufügen. Dann exportieren!

... Dann sieht es so aus:

![](../img/workshop_expl.png)




## Holen wir selber ein DEM-Daten!

https://portal.opentopography.org/raster?opentopoID=OTSRTM.082015.4326.1




## Citation

swiss_dem_example.tif stammt von der Plattform der CGIAR - Consortium for Spatial Information (CGIAR-CSI): 
Jarvis A., H.I. Reuter, A. Nelson, E. Guevara, 2008, Hole-filled seamless SRTM data V4, International Centre for Tropical Agriculture (CIAT), available from
https://srtm.csi.cgiar.org. Accessed: 2024-10-25

Dataset Citation: NASA Shuttle Radar Topography Mission (SRTM)(2013). Shuttle Radar Topography Mission (SRTM) Global.  Distributed by OpenTopography.  https://doi.org/10.5069/G9445JDF. Accessed: 2024-10-25


