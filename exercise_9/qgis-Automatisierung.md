# Automatisierung

## Wofür braucht es "Automatisierung"?
* Geringerer Aufwand durch weniger Nutzerinteraktion
* Weniger Fehler durch Konzeptualisierung a priori
* Modularisierung durch Definition von (Teil-)Abläufen
* Wiederverwendbarkeit/Verschachtelung von Prozeduren
* Geringere Redundanz mittels Wiederverwendbarkeit

![Automatisierung_Schaubild](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/automatisierung.PNG)

## Graphische Modellierung

### Tool öffnen
* das Tool findet ihr unter "Processing" --> "Graphical Modeller"
* Modelnamen festlegen und dann erst einmal speichern

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_modelbuilder_open.mp4"></video>

### Model erstellen und speichern
* Inputs hinzufügen:
  * Layer (Welche Daten werden für die Analyse benötigt?)
  * Parameter (Welche weiteren Einstellungen werden genutzt? z.B. Bufferdistanz, Attributfelder filtern etc.)
* Algorithms auswählen:
  * hier habt ihr Zugriff auf alle QGIS-Tools

* Beispiel: zunächst alle Städte mit einer bestimmten Mindestbevölkerung selektieren, für die Selektion eine Buffer-Operation durchführen mit anpassbarer Buffer-Distanz

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_modelbuilder_model.mp4"></video>

### Model ausführen
* Modelparameter eingeben und Model ausführen
* auf diese Art und Weise kann der gleiche Ablauf schnell und einfach mit angepassten Parametern oder Input-Layern durchgeführt werden

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_modelbuilder_run.mp4"></video>

### Modell exportieren
* Modelle können als Abbildung exportiert werden (z.B. im png-Format). Dies ist sehr hilfreich zur Dokumentation der eigenen Arbeitsschritte.
* auch ein Export in die Programmiersprache python ist möglich

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_modelbuilder_export.mp4"></video>
