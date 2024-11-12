# Verschiedene Daten und Karten einlesen

## Tabelle einlesen!

Okay - Vektordaten einlesen ist ziemlich einfach gewesen!
Kann man sonst andere Daten in QGIS einlesen? Ja!

Hier lesen wir eine Tabelle (Excel-Format).
Wir verwenden als Beispiel diese Daten:

Average age of the permanent resident population by category of citizenship, sex and canton, 2010-2023
https://www.bfs.admin.ch/bfs/en/home/statistiken/bevoelkerung/alterung.assetdetail.32374890.html

Da findet man Durchschnittsalter (nach verschiedenen Faktoren wie Kanton, Jahr, Gender, Ausländer oder nicht).

Die Tabelle kann man auch einfach in QGIS durch Drag&Drop importieren!

Super!

Aber es ist etwas langweilig...
Wir haben doch vorher Kantonsgrenze als Vektordaten importiert. 
Und wir haben hier Durchschnittsalter nach Kanton - Kann man die Beiden kombinieren/fusionieren?
__JA!__

Zuerst schauen wir die Layer von Kantonsgrenze (geoBoundaries-CHE-ADM1)
1. Die Layer in der Spalte links unten klichen
1. Rechts-Klick
1. "Attributtabelle öffnen"
Dann sieht man welche Attribute in dieser Vektordaten zu finden sind. 
... ShapeName, ShapeISO usw.

Und in der Excel-Tabelle (wir nehmen das Jahr 2023) gibt es nur Kantosnamen. 
Weil wir diese beiden Layers sinnvoll kombinieren wollen, sollen wir zuerst eine neue Spalte in der Excel-Tabelle haben, durch die die beiden Tabelle abgeglichen werden können. Hier nehmen wir einfach den Namen.
1. in der Excel-Tabelle eine neue Spalte hinzufügen und beliebig nennen
1. in dieser Spalte soll man die genau identischen Kantonsnamen in Attributttabelle eintragen

Die Tabelle sollte so etwa wie die Excel-Tabelle in `./qgis/data/kanton_age_ave.xlsx` aussehen...
Diese Tabelle in QGIS einlesen.

Dann...
1. Die Layer "geoBoundaries-CHE-ADM1" rechts klick
1. "Eigenschaft" klicken > "Verknüpfungen" klicken > Im Popup-Fenster das "+"-Symbol klicken
1. Ein weiteres Fenster kommt vor. Dort Die zwei Spalte in den beiden Dateien (Excel und geoBoundaries) auswählen, die identische Indikatoren haben > "OK" klicken
1. "Anwenden" klicken > Dann ist die Daten jetzt fusioniert. 

Um die Verknüpfung zu überprüfen, schauen wir zuerst die Attributtabelle von "geoBoundaries". Jetzt ist die Tabelle länger geworden...
Dann können wir je nach Durchschnittsalter Kanton klassifizieren und mit unterschiedlichen Farben malen!
1. Die Layer rechts klick > "Eigenschaften" > "Symbolisierung" klicken
1. Erste Balken "Abgestuft" auswählen > "Wert" eine passende Spalte auswählen > Farbverlauf irgendwas auswählen
1. "Klassifizieren" klicken
1. "Anwenden" klicken

Fertig!

![](../img/test2.png)




