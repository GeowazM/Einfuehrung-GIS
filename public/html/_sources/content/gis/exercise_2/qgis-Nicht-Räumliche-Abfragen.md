# Nicht-Räumliche Abfragen

## Manuelle Auswahl
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_attribute_table.mp4"></video>
* manuell in der Attributtabelle auswählen durch anklicken

## Select by Expression

### Arithmetische Operatoren (Integer, Float-Felder)
* `>`, `<`, `=`, `!=`
* z.B. alle Städte mit mehr als 20 Millionen Einwohnern im Jahr 2015: `"2015" > 20000`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expresion_greater.mp4"></video>

### String Operatoren (Text-Felder)
* `LIKE`
* z.B. alle Länder in Asien: `"continent" LIKE 'asia'`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expression_like.mp4"></video>

* man kann auch `%` als *Platzhalter* nutzen und so nach bestimmten Teilwörtern selektieren
* z.B. alle Länder, welche auf `stan`enden: `"name" LIKE '%stan'`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expression_placeholder.mp4"></video>

### Logische Operatoren
* `AND`, `OR`
* können dafür genutzt werden, verschiedene Abfragen oder Kriterien zu kombinieren
* z.B. alle Städte, welche 1950 noch keine Millionenstadt waren, aber 2015 schon mehr als 10 Millionen Einwohner hatten: `"1950" < 1000 AND "2015" > 10000`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expression_and.mp4"></video>

*Further Resources*
Die QGIS Dokumentation zu logischen Operatoren kann unter folgendem Link gefunden werden:

https://docs.qgis.org/3.10/en/docs/user_manual/working_with_vector/attribute_table.html#selecting-features

## Selektierte Features als neue Datei speichern

* Layer-Properties --> Export --> Save only selected features

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_export.mp4"></video>
