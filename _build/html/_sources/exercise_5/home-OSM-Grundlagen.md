# OSM Grundlagen

OSM, kurz für OpenStreetMap, ist eine frei nutzbare Geodatenbank die von jeder Person editiert und erweitert werden kann.
Mehr zu OSM und wie man in OSM kartiert könnt ihr unter https://learnosm.org/de/ finden.

## OSM-Account anlegen

Unter https://www.openstreetmap.org/user/new könnt ihr einen OSM-Account anlegen.

## In OSM mappen

Um in OSM mappen zu können müsst ihr erst auf einen noch nicht oder unvollständig kartierten Bereich hineinzoomen.
Wenn der `edit` Knopf noch ausgegraut ist, ist der gewählte Ausschnitt zu groß.

![OSM Kartenansicht](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/startseite.png) ![OSM Kartenansicht, reingezoomt](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/hassilabied-osm.png)

Hat man einen Auschnitt gewählt, kann man auf den `edit` Knopf drücken und es öffnet sich das Kartierfenster.

Bei der ersten Session mit einem neuen Account schlägt die Webseite dem Benutzer eine kurze Demonstration der Funktionen vor, macht diese gerne durch um eine Idee vom Kartieren in OSM zu bekommen!

![OSM Kartierfenster](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/hassilabied-satellit.png)

Über dem Satellitenbild werden die schon gemappten Objekte angezeigt, ihr seht also auch in der Kartieransicht welche Objekte schon kartiert sind und welche nicht.

Wenn ihr ein Objekt gewählt habt, dass ihr mappen wollt, müsst ihr entscheiden, ob es am Besten als ein Punkt-, Linien- oder Flächenobjekt dargestellt wird.
Diese drei Objekttypen stehen für die Kartierung in OSM zur Verfügung.

Wenn alle Objekte kartiert sind, auf `upload` klicken und einen Changeset Kommentar schreiben der kurz zusammenfasst was ihr geändert habt, dann speichern.

### Punkte

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/videos/map-trees.mp4"></video>

- Klick zum Setzen eines Punktes
- Feature Typ wählen
- Felder nach bestem Wissen ausfüllen

### Linien

Linienobjekte in OSM setzen sich aus mehreren miteinander verbundenen Punkten zusammen.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/videos/map-road.mp4"></video>

- Klick zum Setzen der Punkte
- Doppelklick auf letzten Punkt zum Beenden der Linie
- *falls notwendig:*
  - Rechtsklick auf letzten Punkt um die Linie fortzuführen
- Feature Typ wählen
- Felder nach bestem Wissen ausfüllen

### Flächen

Flächenobjekte in OSM sind eigentlich nur geschlossene Linienobjekte.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/videos/map-house.mp4"></video>

- Klick zum Setzen der Punkte
- Klick auf den ersten Punkt zum Schließen der Fläche
- *falls notwendig:*
  - Rechtsklick in die Fläche um rechte Winkel zu setzen
- Feature Typ wählen
- Felder nach bestem Wissen ausfüllen

### Attribute von OSM Objekten anpassen

Um Attribute von OSM-Objekten zu verändern oder hinzuzufügen, müsst ihr ebenfalls in dem `edit`Fenster arbeiten.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/videos/edit-tags.mp4"></video>

- Klick auf das Objekt das angepasst werden soll
- Das Attribut (auch "Tag" genannt) anpassen

## How to Abgabe: Changesets

Um eure Änderungen in OSM nachvollziehen zu können brauchen die Korrektoren euren OSM Nutzernamen und die Changeset ID eurer Änderungen.

Die Changeset ID wird euch direkt nach dem Upload eurer Änderungen angezeigt, aber ihr könnt sie auch unter eurem Konto `My Profile` > `My Edits` zu jedem Upload den ihr gemacht habt finden.

![Changeset ID unter "My Edits"](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/OSM/changeset-id.png)

## Weitere Wege zu OSM beizutragen

### HOT (Humanitarian OSM Team) Tasking Manager

Der Tasking Manager ist ein Werkzeug für die Koordination von Freiwilligen und Organisation von Gruppen zur Kartierung in OpenStreetMap.
Der Zweck des Tools besteht darin, eine Kartierungsaufgabe in kleinere Aufgaben zu unterteilen, die schnell erledigt werden können. 
Es zeigt, welche Bereiche kartiert werden müssen und in welchen Bereichen die Kartierung validiert werden muss. 
Dieser Ansatz erleichtert die Verteilung der Aufgaben an die verschiedenen Kartierer. 
Es ermöglicht weiter auch die Kontrolle des Fortschritts und der Homogenität der Arbeit (d. h. abzudeckende Elemente, zu verwendende spezifische Tags usw.).

Die Wurzeln des Tasking Managers liegen in Kartierungskampagnen nach großen Katastrophen (Erdbeben in Haiti, Taifun Haiyan, Erdbeben in Ghorka). Mit seiner Hilfe konnten viele tausend Freiwillige weltweit online koordiniert und dringend benötigte Kartendaten der betroffenen Regionen zur Verfügung gestellt werden.


Der Tasking Manager ist unter folgender Adresse erreichbar:

https://tasks.hotosm.org/

Ihr könnt euch auf der Webseite mit eurem OpenStreetMap Account anmelden.

Wählt dann ein Kartierungs Projekt aus. Ihr könnt z.B. nach Schwierigkeitsgrad und Dringlichkeit oder auch Themengebiet(Disaster, Nachhaltigkeit) filtern. 
Manche Projekte setzen Erfahrung vorraus. Dazu müsst ihr eine gewisse Anzahl an tasks erledigt haben.
**Wichtig** lest die Anweisungen und Tipps des Projektes zu dem Ihr beitragen wollt.

Wenn ihr ein Projekt und eine Task ausgewählt habt werdet ihr auf die üblichen OSM Editoren verlinkt (z.B. iD). 
Dort kartiert ihr in dem vorgegebenen Bereich (der Task). 
Wenn ihr fertig seid und eure erstellten Daten auf OpenStreetMap hochgeladen habt, kehrt zur Tasking Manager website zurück. 
Im Tasking Manager habt ihr für euren ausgewählten Task die folgenden Optionen:

* Aufgabe speichern - Ihr seid fertig mit dem kartieren der Task. Vergesst nicht einen Status festzulegen: _Ist diese Aufgabe vollständig kartiert?_
  - **Ja** - Alle vom Projekt vorgegebenen Objekte (z.B. Gebäude & Straßen) innerhalb des Gebietes sind kartiert
  - **Nein** - Es sind noch Objekte im Gebiet vorhanden die nicht kartiert wurden, Ihr möchtet aber nicht weiter kartieren bzw. eine andere Aufgabe bearbeiten
* Aufgabe aufteilen - das Gebiet erscheint euch zu groß bzw. es beinhaltet zu viele Objektsignaturen (z.B. Gebäude in urbanen Regionen)
* Eine andere Aufgabe wählen - wählt eine andere Aufgabe ohne zu speichern.



### Mapillary - Kartieren mittels Streetlevel Bildern

Viele relevante Geoobjekte sind auf frei verfügbaren Satellitenbildern nur schwer oder nicht zu erkennen.
Dazu zählen z.B. Verkehrsschilder, Schranken, Straßenlaternen, öffentliche Briefkästen oder die Oberfläche von Straßensegmenten.


**Mapillary** ist eine Platform und Software zum aufnehmen und verteilen von sogenannten Streetlevel Bildern (vgl. Google Streetview).
Per App/Website können Fotos auf die Platform hochgeladen werden. 
Dise Fotos werden Georeferenziert und auf einer Karte abgebildet. 
Nutzer können diese Fotos dann nutzen um sich eine Region aus on-the-ground Perspektive anzusehen.
Weiter können diese Fotos auch genutzt werden um Objekte in OpenStreetMap beizutragen.

Website: https://www.mapillary.com
Platform: https://www.mapillary.com/app

**Mapillary nutzen um auf OSM beizutragen**

Geht auf die Platform Website und zoomt in eine Region eures Interesses. 
Wählt ein Bild aus (Klick auf einen Grünen Punkt in der Karte).
Rechts seht ihr ein Symbol mit 3 Punkten, die _Image Details_.
Dort findet Ihr einen link zu drei OSM Editoren. 
Wählt iD aus.
Der iD Editor öffnet sich inklusive einem Mapillary Overlay.
Nun könnt ihr ganz herkömmlich OSM editieren und habt sowohl die Satelliten als auch die Streetlevel Perspektive.

#### Verbessert Radwege routing!

Ihr fahrt gerne Rennrad, aber seid mit den Routen von Komoot/Strava/Garmin/Outdooractive nicht immer happy, da z.B. zu viel Schotter oder Waldwege eingebaut werden. 
Alle diese Dienste nutzen OSM als Grundlage. 
Oberflächentyp und Smoothness könnt ihr in OSM direkt hinzufügen/verbessern. Wenn ihr die Wege nicht selbst kennt, nutzt Mapillary wenn Fotos vorhanden sind oder nehmt Sie selbst per Mapillary App auf.


### Microtasks mit Streetcomplete

Streetcomplete ist ein Einsteigerfreundlicher OpenStreetMap Editor für Android Smartphones und Tablets zum kartieren unterwegs.

https://streetcomplete.app/?lang=en

Die App zeigt Orte, an denen Daten über die App zu OpenStreetMap hinzugefügt werden können, als Quest-Pins auf einer Karte an. 
Jede dieser Aufgaben kann durch die Beantwortung einer einfachen Frage gelöst werden, wie z.B. 
"Ist diese Straße beleuchtet?". 
Die gegebenen Antworten werden dann verarbeitet und direkt in die OSM-Datenbank im Namen des OSM-Kontos des Benutzers hochgeladen.
Im Gegensatz zu den meisten anderen OSM-Editoren werden die eigentlichen Daten also nicht direkt auf der Karte angezeigt und es kann auch keine Geometrie verändert werden (mit Ausnahme der Aufteilung von Wegen). 
Der Beitrag zu dieser App erfolgt in erster Linie durch die Beantwortung dieser Aufgaben.


