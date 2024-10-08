# Geodaten in QGIS öffnen

QGIS organisiert wie die meisten Geoinformationssysteme Daten in Form von Layern. Ein Layer repräsentiert einen Datensatz (oder einen Teil eines Datensatzes). Um Daten in QGIS zu laden, muss man daher einen neuen Layer erstellen.

## Welche Layer-Arten gibt es?
* in der Kartographie Übung werden wir uns fast ausschließlich mit **Vektor** und **Geo-Package** Layern beschäftigen
* in der Einführung in die Geoinformatik werden auch  **Raster** und **Delimited Text** Layer eine wichtige Rolle spielen
* weiterführende Veranstaltungen (z.B. Seminar Geodatenbanken oder Web-Mapping) geben Einblicke für **SpatialLite**, **PostgreSQL**, **WMS**, **WFS**

![layer_types](https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/img/layer_types.png)

*Abbildung 1: Verschiedene Layer-Arten in QGIS*

## Vektor-Layer öffnen
* Vektordateien haben zum Beispiel folgende Endungen: `.geojson`, `.shp`, `.kml`, `.gpx`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/qgis_open_vector.mp4"></video>
* Man kann Vektordateien auch öffnen indem man die Datei per *Drag&Drop* in die Kartenansicht "zieht" und "abwirft".
* Ein Einfügen über den Browser in QGIS ist zudem auch möglich (per *Drag&Drop* oder Doppelklick).

## Geopackage-Layer öffnen

Ein Geopackage kann mehrere Datensätze enthalten, die einzeln geladen werden können.
Die Abbildung zeigt den entsprechenden Dialog. Nachdem über *Connect* eine Verbindung zum Geopackage hergestellt wurde, können einzelne Datensätze ausgewählt und geladen werden. Falls mehrere Geopackages verbunden sind, muss das gerade neu verbundene Geopackage nochma in der Liste ausgewählt werden.

![Geopackages über Add Layer hinzufügen](https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/img/geopackagesAddLayer.png)

Komfortabel ist die Möglichkeit, Geopackages über das *Browser*-Panel zu verwalten, das separat aktiviert werden muss (s. [Fenster und Toolbars hinzufügen](GUI)). Hier werden alle verbundenen Geopackages angezeigt und einzelne Datensätze können über Doppelklick oder Drag & Drop als Layer dem Projekt hinzugefügt werden.
![Geopackages über das Browser Panel laden/verwlaten](https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/img/geopackageBrowser.png)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/QGIS_geopackageLadenAddLayer.mp4"></video>
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/QGIS_geopackageLadenBrowser.mp4"></video>
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/QGIS_geopackageLadenDragDrop.mp4"></video>
## Raster-Layer öffnen
* Rasterdateien haben zum Beispiel folgende Endungen: `.tif`, `.tiff`, `.geotiff`, `.ascii`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/qgis_open_raster.mp4"></video>
* Man kann Rasterlayer auch öffnen, indem man sie im Browserfenster in QGIS per Doppelklick auswählt oder von hier aus per *Drag&Drop* in die Kartenansicht "zieht".

## Text-Layer öffnen
* Textdateien, welche Informationen in Tabellenform enthalten, haben zum Beispiel folgende Endungen: `.csv`, `.xlxs`
* wichtig ist hierbei, dass mindestens eine Spalte die Geometrie bzw. Koordinaten enthält
* für Punkte gibt es in der Regel jeweils eine Spalte für *Latitude* und *Longitude*

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/qgis_open_textfile.mp4"></video>