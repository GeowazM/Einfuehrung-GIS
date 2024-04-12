# Benutzeroberfläche anpassen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_move.mp4"></video>

## Übersicht
![QGIS Interface](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/gui_numbered.png)
**1) Layers List / Browser Panel**  
Die Layer-Liste zeigt alle Layer/Dateien an, die im Projekt geladen sind. Man kann Layer einblenden/ausblenden und weitere Eigenschaften einstellen.  

**2) Toolbars**  
Toolsbars sind *Shortcuts* um besonders häufig genutze Befehle auszuführen. So gibt es beispielsweise spezielle Toolbars für Vektor und Rasterdateien, aber auch allgemeine um z.B. euer Projekt zu speichern etc.  
In der Toolbar befindet sich unter anderem auch die Toolbox (Werkzeugkasten), welche in vielen der Wiki-Videos später verwendet wird.
![Geschlossene_Toolbox_01](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis//uploads/af1744d7b9694df4605f5f3e9bd8906b/Geschlossene_Toolbox_01.png)

**3) Kartenansicht**  
Die Kartenansicht ist der zentrale Bestandteil jedes GIS Programms. Hier werden die Geodaten angezeigt. Die Kartenansicht hat eine Projektion, welche nicht immer mit der Projektion der Layer übereinstimmen muss.

**4) Status-Leiste**  
In der Status-Leiste findet ihr zentrale Informationen zur aktuellen Kartenansicht. Hier stellt ihr die Projektion der Kartenansicht ein und den Maßstab. Ihr könnt die Koordinaten des Mauszeigers ablesen und so schnell die Koordinaten von Punkten auf der Karte herausfinden. Ihr könnt eure Kartenansicht drehen, z.B. wenn ihr eine nach Süden ausgerichtete Karte erstellen möchtet.

**5) Side Toolbar**  
Möglicherweise wird euch eine Seitenleiste angezeigt. Diese stellt einen weiteren Weg dar, Vektor und Raster-Dateien auf einfache Art und Weise in QGIS zu öffnen.

**6) Locator bar**  
Hier könnt ihr nach Tools und Layer suchen. Wenn ihr nicht wisst, wo ihr ein Tool findet, könnt ihr es hier probieren.

## Verschieben der Kartenansicht
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_move.mp4"></video>

* man kann auch mit den *Pfeiltasten* verschieben

## Zoomen in der Kartenansicht
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_zoom.mp4"></video>{width=80}

* man kann auch durch *Scrollen* Zoomen
* oder mit `Ctrl+` bzw. `Ctrl-`

## Eigenschaften von Objekten anzeigen
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_identify.mp4"></video>

## Projektion der Kartenansicht einstellen (Projekt-KBS)
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_map_projection.mp4"></video>

## Projekt speichern und öffnen
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_save_project.mp4"></video>

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_open_project.mp4"></video>

**Hinweis:**  
Die im Projekt verwendeten Layer-Daten werden nicht in der Projekt-Datei gespeichert. Stattdessen enthält die Projekt-Datei lediglich die Dateipfade, wo sich die Layer-Daten zum Zeitpunkt der letzten Abspeicherung des Projekts auf dem PC befunden haben. Sollte der Speicherort dieser Layer-Daten nachträglich verändert werden, kommt es bei erneuter Öffnung des Projektes zur Fehlermeldung "nicht verfügbare Layer behandeln".
Eine gute [Datenorganisation](/exercise_1/arbeiten_mit_qgis/home-Datenorganisation) mit einer festen und durchdachten Ordnerstruktur verhindert solche Probleme.

<video controls style="max-width: 80%;">
  <source src="/uploads/5b05bfc35c0926253110d15c339e3c2e/Anzeigen_einblenden_ausblenden.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


## Anzeigen ein- und ausblenden
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/5b05bfc35c0926253110d15c339e3c2e/Anzeigen_einblenden_ausblenden.mp4"></video>

## Toolbars verschieben und anordnen
An jeder Toolbar gibt es ein Feld aus zwei gepunkteten Linien. Wenn man mit dem Mauszeiger hinüberfährt bis ein Pfeilkreuz erscheint und dann die linke Maustaste gedrückt hält, kann man die Toolbar verschieben. Dies ermöglicht eine individualisierte Anordnung der eigenen Werkzeuge. Durch die Komprimierung aller Toolbars in wenige Zeilen kann zudem noch das Fenster der Kartenansicht vergrößert werden.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/aa78e6cfe73b2c517fbee01a45b8229c/Toolbar_verschieben.mp4"></video>

## Erweiterungen installieren  
Für QGIS gibt es zahlreiche Erweiterungen, auch *Plugins* genannt, die erweiterte Funktionalitäten zur Verfügung stellen.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_plugins.mp4"></video>

**Hinweis:**  
Solltet ihr eine spezifische Erweiterung nicht finden, überprüft eure Groß-/Kleinschreibung und die korrekte Verwendung von Leerzeichen. Sollte eine Erweiterung weiterhin nicht auffindbar sein, müssen eventuell die experimentellen Erweiterungen in den Optionen erlaubt werden (siehe unten).

## Erweiterungen verwalten
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/4b17e06f642578e99df1399b055197c1/Erweiterungen_verwalten.mp4"></video>

## Experimentelle Erweiterungen erlauben
Experimentelle Erweiterungen sind entweder noch in der Entwicklung, oder es handelt sich um veraltete Erweiterungen, die nicht mehr für die neueren Versionen von QGIS weiter optimiert/angepasst werden. Trotzdem kann die Verwendung experimenteller Erweiterungen sinnvoll sein:  
* Spezifische Funktionen werden in keiner anderen Erweiterung unterstützt.  
* Alternative, wenn es bei einer anderen Erweiterung zu Problemen kommt.  
* Ein Tutorial greift auf eine bestimmte Erweiterung zurück.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/7835bdcccb4e967e6599eb46ce936bf6/Experimentelle_Erweiterungen.mp4"></video>

**Hinweis:**  
Aufgrund der oftmals fehlenden Optimierung für die verwendete QGIS-Version, kann es bei experimentellen Erweiterungen vermehrt zu Fehlermeldungen oder anderen Problemen bis hin zum Absturz von QGIS kommen. Experimentelle Erweiterungen sollten daher sicherheitshalber nur für die Verwendung aktiviert und anschließend wieder deaktiviert werden. Vergewissert euch zusätzlich, dass der aktuelle Arbeitsfortschritt gespeichert ist, um einem Datenverlust beim Absturz von QGIS zu entgehen.

# Weitere Ressourcen
* [QGIS-Doku: An Overview of the Interface](https://docs.qgis.org/3.4/de/docs/training_manual/introduction/overview.html)
