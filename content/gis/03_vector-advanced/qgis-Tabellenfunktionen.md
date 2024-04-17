# Tabellenfunktionen


## Add Field
* Ein Feld zur Attributtabelle hinzufügen
* Achtung: je nachdem welche Information ins Attributfeld eingetragen werden soll, muss der richtige Datentype gewählt werden
* Beispiel: Ein Feld für die *Bevölkerungsdichte* hinzufügen, Datentyp: Float oder Double oder Real (Gleitkommazahlen)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_add_field.mp4"></video>

## Delete Field
* Ein Feld aus der Attributtabelle löschen
* Beispiel: alle ungenutzen/unnötigen Felder aus dem Layer löschen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_delete_field.mp4"></video>

## Calculate Field
* Die Attributwerte für ein Feld berechnen, z.B. anhand den Werten von anderen Feldern
* in QGIS kann ein neues Feld erstellt werden oder ein bestehendes Feld aktualisiert werden
* Achtung: Überprüft, ob der Datentyp des Feldes und eurer Berechnung zusammenpassen. Berechet ihr ein Verhältnis (z.B. eine Dichte), so sollte das Feld beispielsweise nicht den Typ *Integer* (Ganzzahl) haben
* Beispiel: Die *Bevölkerungsdichte* anhand der schon bestehenden Felder *Bevölkerungszahl* und *Fläche* berechnen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_calculate_field.mp4"></video>

## Basic Statistics for Fields
* generiert eine Statistik für ein bestimmtes Feld in der Attributtabelle
* Beispiel: Statistik für das Feld Bevölkerungsdichte für alle Länder, was ist der Maximalwert, Durchschnitt, etc.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_field_stats.mp4"></video>

## Statistics by Categories
* aggregierte Statistiken für Kategorien erstellen
* Für welche Felder in der Attributtabelle sollen Statistiken berechnet werden?
* welches Feld in der Attributtabelle enthält die Kategorie?
* Beispiel: Wie viele Städte mit mehr als 300,000 Einwohner gibt es pro Land? Für jedes Land: wie viele Menschen leben in der größten Agglomeration?

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_stats_by_category.mp4"></video>
