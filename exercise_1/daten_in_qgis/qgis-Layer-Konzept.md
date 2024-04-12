# Layer-Konzept

## Welche Layer-Arten gibt es?
* in der Einführung werden wir uns mit **Vektor**, **Raster** und **Delimited Text** Layer beschäftigen
* weiterführende Veranstaltungen (z.B. Seminar Geodatenbanken oder Web-Mapping) geben Einblicke für **SpatialLite**, **PostgreSQL**, **WMS**, **WFS**

![Layer-Arten](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/layer_types.png)

*Abbildung 1: Verschiedene Layer-Arten in QGIS*

## Vektor-Layer öffnen
* Vektordateien haben zum Beispiel folgende Endungen: `.geojson`, `.shp`, `.kml`, `.gpx`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_open_vector.mp4"></video>

* Man kann Vektordateien auch öffnen indem man die Datei per *Drag&Drop* in die Kartenansicht "zieht" und "abwirft".
* Ein Einfügen über den Browser in QGIS ist zudem auch möglich (per *Drag&Drop* oder Doppelklick).

## Raster-Layer öffnen
* Rasterdateien haben zum Beispiel folgende Endungen: `.tif`, `.tiff`, `.geotiff`, `.ascii`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_open_raster.mp4"></video>

* Man kann Rasterlayer auch öffnen, indem man sie im Browserfenster in QGIS per Doppelklick auswählt oder von hier aus per *Drag&Drop* in die Kartenansicht "zieht".

## Text-Layer öffnen
* Textdateien, welche Informationen in Tabellenform enthalten, haben zum Beispiel folgende Endungen: `.csv`, `.xlxs`
* wichtig ist hierbei, dass mindestens eine Spalte die Geometrie bzw. Koordinaten enthält
* für Punkte gibt es in der Regel jeweils eine Spalte für *Latitude* und *Longitude*

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_open_textfile.mp4"></video>

## Layer ausblenden und einblenden
* in der *LayerToolbar* Häkchen setzen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_show_hide_layer.mp4"></video>

* habt ihr euer Layer "verloren"? *Rechtsklick --> Zoom To Layer*

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_zoom_to_layer.mp4"></video>

## Layer in der Hierarchie verschieben
* in der *LayerToolbar* nach oben und unten verschieben
* ein Layer ganz nach oben bringen: *Rechtsklick --> Move To Top*

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_layer_hierarchy.mp4"></video>

## Layer Namen ändern
* *Rechtsklick --> Rename*

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_rename_layer.mp4"></video>

## Layer Eigenschaften
Jedes Layer hat zusätzliche Eigenschaften, die ihr einsehen und anpasen könnt. An dieser Stelle betrachten wir zunächst nur die folgenden:
### Information
* eine Übersicht zu Layer-Name, Dateiformat, Speicherort, räumliche Ausdehnung, Anzahl der Features (Objekte),...

### Symbology
* Darstellungsweise des Layers, Style, Transparenz

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_layer_properties.mp4"></video>

# Weitere Ressourcen
* [QGIS-Doku: Adding your first layer](https://docs.qgis.org/3.4/de/docs/training_manual/introduction/preparation.html)
