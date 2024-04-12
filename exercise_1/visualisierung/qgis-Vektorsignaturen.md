# Vektorsignaturen
Die kartographische Darstellung von Vektor-Layern im GIS ist ein weites und komplexes Themenfeld. Wir betrachten hier daher nur einige grundlegende Funktionen.  

**Hinweis:**  
Die getätigten Veränderungen bei der Darstellung eines Layers werden nur lokal in eurer Projektdatei gespeichert und nicht in der Layer-Datei direkt. Wird die Layer-Datei also außerhalb eures Projektes geöffnet (zum Beispiel wenn ihr sie als Teil einer Abgabe in Moodle hochgeladen habt), sind die Darstellungseinstellungen verloren.  
Ihr könnt die Darstellung jedoch getrennt als Datei abspeichern (siehe [Signaturen speichern und laden](/exercise_1/visualisierung/qgis-Vektorsignaturen.md#signaturen-speichern-und-laden)). Für die Abgaben empfehlen sich aber stattdessen Screenshots in der Dokumentation.

## Single Symbol
* alle Features im Layer werden auf die gleiche Art und Weise (Farbe, Größe, etc.) dargestellt
* Rechtsklick auf Layer --> Symbology --> Single Symbol

### Farbe ändern
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_change_color_point.mp4"></video>

### Größe ändern
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_change_size_point.mp4"></video>
* diese Einstellung gibt es nur für Punkte und Linien

### Punkt-Icon ändern
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_change_icon_point.mp4"></video>
* auch für Linien könnt ihr unterschiedliche bestehende Styles wählen

### Polygon Füllung ändern
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_change_polygon_fill.mp4"></video>
* auch hier könnt ihr unterschiedliche bestehende Styles wählen

### Transparenz einstellen
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_layer_opacity.mp4"></video>

## Nominale Daten - Categorized
* alle Feature einer Kategorie sollen auf gleiche Art und Weise dargestellt werden
* Rechtsklick auf Layer --> Symbology --> Categorized
* für jede Kategorie kann die Darstellung angepasst werden (auf ähnliche Art und Weise wie im Abschnitt *Single Symbol* dargestellt)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_symbology_categorized_polygon.mp4"></video>

## Intervallskalierte Daten - Graduated
* Features sollen entsprechend einer Skala dargestellt werden
* Darstellung über Farbverlauf oder Größe
* Daten werden in Klassen eingeteilt nach einer bestimmten Methode (z.B. `equal interval` oder `equal count`) oder manuell
* Für jede Klasse kann die Darstellung angepasst werden (auf ähnliche Art und Weise wie im Abschnitt *Single Symbol* dargestellt)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_symbology_graduated_point.mp4"></video>

## Signaturen speichern und laden
In QGIS könnt ihr die Signaturen auch als Datei speichern und so für verschiedene Projekte und Layer nutzen.
* Rechtsklick auf Layer --> Export --> Save as QGIS Layer Style File

Für ein neues Layer könnt ihr dann die Signatur wie folgt laden, möglicherweise müsst ihr dann noch den Namen des Feldes mit den Attributen anpassen.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_symbology_load_style.mp4"></video>

## Beschriftung
* jedes Feature kann mit Werten aus der Attributtabelle beschriftet werden
* Rechtsklick auf Layer --> Labels

### Automatische Platzierung
* automatische Platzierung von Labels funktioniert manchmal nur semi-optimal, geht dafür aber sehr einfach und schnell

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_labels.mp4"></video>

### Manuelle Platzierung
* man startet mit einer automatischen Platzierung und passt dann die Position manuell an
* ermöglicht kartographisch besser platzierte Label, nimmt aber oft sehr viel Zeit in Anspruch
* Nutzung der *Labeling Toolbar*

![labeling_toolbar](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/labeling_toolbar.PNG)


<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_labels_by_hand.mp4"></video>

---
# Weitere Ressourcen
* [QGIS Doku: Symbology](https://docs.qgis.org/testing/en/docs/training_manual/basic_map/symbology.html)
