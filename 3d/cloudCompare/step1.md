# CloudCompare - Step 1


Dieses Anleitung ist von [龍泉Ⅲ](https://ameblo.jp/arciwasa/entry-12652714120.html) erstellt.

In dieser Anleitung geht es darum, die Inschriften leserlich zu machen.

Zuerst das Modell (PLY-Format) herunterladen:
"野崎字　駐車場整備　墓碑" (https://skfb.ly/6YwIW) by tiwasa is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

... Wenn man keinen Account von Sketchfab hat, kann man das Modell von `../data/inschrift.ply` herunterladen.
Wenn das Modell auf dem PC/Mac herunterladen ist, dann dies bitte in CloudCompare öffenen.

## Modell ist da. Was tun?

Objekt markieren => Erfolgt in DBTree (Fenster links oben)
Drag mit Mouse-links => Modell Drehen
Drag mit Mouse-Rechts => Modell bewegen

Weiteres schauen wir im Workshop...

Zum Beginn der Verarbeitung des Modells - in CloudCompare gibt es keinen "Rückgängig machen"-Button.
Deshalb ist es vielleicht sinnvoll, das Modell "clonen" (Das Schäfchen-Symbol klicken)

1. Farbskala nach Z-Ache vergeben

    `Edit > Colors > Height Ramp`
    Dadurch wird die Farbverlauf nach der Tiefe/Z-Achse verleiht.

1. Modell vergrössern

    Mit `Edit > Scale/Multiply` kann man die Grösse des Modells ändern.
    - Man kann es alle 3 Richtungen (XYZ) gleichmässig vergrössern.
    - Oder in beliebige Richtungen beliebig gross... 

    In diesem Fall wäre es interessant, wenn das Modell in die Tiefe (Z-Achse) tiefer machen könnte.

1. Filtern einsetzen
    
    Es sind 2 Filters, [Eye-Dome Lighting (EDL)](https://viscircle.de/eye-dome-lighting-eine-nicht-fotorealistische-shading-technik/) und [Screen Space Ambient Occlusion (SSAO)](https://en.wikipedia.org/wiki/Screen_space_ambient_occlusion) oben rechts verfügbar. Die beiden Filter dienen dazu, die Tiefeninformation der 3D-Szene zu verdeutlichen.

1. Mit Lichtquelle bearbeiten

    Um die Licht/Schatten-Darstellung wirksam zu machen, berechen wir zuerst die Normale. 
    1. `Edit > Normals > Compute` klicken
    1. Im Popup berechnen "per-vertex" auswählen

    Wenn die Normale ausgerechnet sind, kann man Sonnenlicht (die Lichtquelle, die sich nicht bewegt) mit F6 und Custom Licht (Lichtquelle, die man bewegen kann) mit F7 ein/ausschalten.

    Wenn das Custom Licht aktiviert ist, erscheint eine gelbe Kreuz irgendwo in der Szene. Die kann man mit Ctrl/CMD + Rechts-Mouse-Drag bewegen.

1. Noch eine Möglichkeit ShadeVis (plugin)

Das Plugin "ShadeVis" realisiert PCV (Portion de Ciel Visible). Nähere Erläuterung in [Wiki von CloudCompare](https://www.cloudcompare.org/doc/wiki/index.php/ShadeVis_(plugin))







