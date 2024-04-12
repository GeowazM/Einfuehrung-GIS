## Hinweise

Die Datei `readme.md` jeder Abgabe enthält genaue Vorgaben, wie die jeweilige Abgabe zu finalisieren und auf Moodle hochzuladen ist. Für alle Abgaben übergreifend gilt:

* Benutzt zweckmäßige Namen!
  -  Die `.pdf`-Datei, welche die einzelnen Schritte eures Workflows dokumentiert, wird mit `Dokumentation.pdf` benannt
* Ergebnisdaten in einem räumlichen Format (Shapefile, GeoPackage, GeoJSON):
  - nicht: `data.gpkg`, `input.gpkg`, `osm_water(3).gpkg`, `finaler_layer.gpkg`
  - besser: `osm_gebaeude_centroids.gpkg`, `natural_earth_adm0_grenzen.gpkg`, `rnv_isochronen_UTM32.gpkg`
* Wenn als Abgabe eine `.zip`-Datei gefordert ist, packt **nur** die für die Abgabe relevanten Dateien in **eine** `.zip`-Datei; insbesondere nicht (!) die unveränderten Input-Daten.
* Bennent die `.zip`-Datei passend: `Abgabe0X_Musterfrau_Erika.zip`
* Solltet ihr Ergebnisdaten im Shapefile-Format abgeben, müsst ihr unbedingt darauf achten, alle Teil-Dateien abzugeben. Das sind:
`.shp`, `.shx`, `.prj`, `.dbf`, `cpg`


Für Abgabe 1 ist lediglich eine `.pdf`-Datei erforderlich. Es ist nicht notwendig die `.pdf`-Datei zu komprimieren oder zu zippen. Bennent die `.pdf`-Datei wie folgt: `Nachname_Vorname_Karte.pdf`, z.B. `Musterfrau_Erika_Karte.pdf`


## Video Tutorials (Windows)


### Dateien Umbenennen
Um eine Datei umzubenennen, markiert Sie in eurem File Explorer oder anderem Dateimanager per Maus und einem Linksklick. Wählt im erscheinenden Kontextmenü `Umbenennen`. Markierte Dateien können auch per Taste [F2] umbenannt werden.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/aa54322c9bb4908ca2152cff5ed879ae/umbennen.mp4"></video>


### Dateien komprimieren/ zippen
Um eine oder mehrere Dateien zu komprimieren / zippen markiert die entsprechende(n) Datei(en) in eurem File Explorer oder anderem Dateimanager per Maus und einem Linksklick. Über den Eintrag _Senden an_ im Kontextmenü wählt `ZIP-komprimierter Ordner`. Alle markierten Dateien werden daraufhin in eine komprimierte `.zip`-Datei überführt.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/7a6300cd4b1dc7172d5cfd01d2225085/zipping.mp4"></video>

### Hochladen auf Moodle
Das Hochladen auf Moodle erfolgt über den [GIS-Kurs in Moodle](https://moodle.uni-heidelberg.de/course/view.php?id=12875). Die Sektion [_Übung: Abgaben_](https://moodle.uni-heidelberg.de/course/view.php?id=12875&section=12) befindet sich am unteren Ende des Kurses. Sie beinhaltet 5 Untersektionen, eine für jede Abgabe. Per Klick auf das entsprechende Menü öffnet sich eine Seite mit weiteren Infos zur jeweiligen Abgabe, dem Link zum entsprechenden GitLab-Ordner und den Bewertungskriterien. Über den Button _Abgabe hinzufügen_ kann per Drag & Drop oder per Klick auf das Dateisymbol (oben links, es öffnet sich ein Kontextmenü zur Auswahl von Dateien auf eurem lokalen PC) eure Abgabe hochgeladen und damit erfolgreich eingereicht werden.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/7ad454512de5d5b9beef258fb6401db3/moodle_submission.mp4"></video>
