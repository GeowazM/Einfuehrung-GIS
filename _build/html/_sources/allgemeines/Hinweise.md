# Hinweise zur Verwendung von GIS-Software
Anfänglich kann das Arbeiten mit GIS Programmen sehr komplex wirken. Gerade wenn man bisher nur wenige Berührungspunkte mit Computer-Software hatte, erscheinen die vielen Optionen und Möglichkeiten des Programms vielleicht eher überwältigend und abschreckend.  
Die folgenden Hinweise sollen daher dazu dienen, einen möglichst unproblematischen Einstieg in das Arbeiten mit QGIS zu ermöglichen, indem bereits auf einige, häufig zu Problemen führenden, Themen eingegangen wird.

## Systemsprache Englisch
Es wird empfohlen die Sprache von QGIS auf Englisch umzustellen. Dies hat mehrere Gründe:  
* Die Wiki-Videos verwenden eine englische Benutzeroberfläche.  
* In den Tutorien wird meist die englische Bezeichnung der Werkzeuge verwendet.
* Externe Tutorials und Foreneinträge sind größtenteils auf Englisch.  

Wie man die Sprache von QGIS umstellt, wird in den [grundlegenden Einstellungen](home-Grundlegende Einstellungen) gezeigt.

## Regelmäßiges Abspeichern
GIS-Programme sind leider dafür berüchtigt, auch gerne mal einzufrieren oder ganz abzustürzen. Zwar ist ein Trend zu erkennen, dass die Komplikationen mit besserer Hardware weniger werden, trotzdem ist selbst ein "Gaming-PC" für mehrere tausend Euro nicht vollkommen davor sicher. Um möglichst keinen Fortschritt an euren Projekten zu verlieren, wird ein regelmäßiges Abspeichern empfohlen (siehe [Projekt speichern und öffnen](qgis-Interface#projekt-speichern-und-öffnen)). Besonders aufwändigere Tasks mit längeren Berechnungszeiten sind anfällig. Daher sollte speziell vor deren Durchführung immer eine Abspeicherung erfolgen.

## GRASS-Anwendungen
QGIS ist eine Ansammlung von verschiedenen Werkzeugen, mit denen Daten bearbeitet und visualisiert werden können. Dabei erlaubt QGIS auch die Verwendung von Werkzeugen externer GIS-Softwares, wie etwa [GRASS GIS](https://grass.osgeo.org/). GRASS muss nicht extra heruntergeladen werden, sondern wird bei der Installation von QGIS automatisch mitinstalliert. GRASS-Werkzeuge sind durch ihr [Icon](https://grass.osgeo.org/images/logos/grassgis_logo_colorlogo_text_whitebg.png) gekennzeichnet. Zusätzlich beginnen die Werkzeug-Bezeichnungen entweder mit _v._ (Vektorwerkzeug) oder _r._ (Rasterwerkzeug).  

Es gilt zu beachten, dass beim Starten der standardmäßigen QGIS-Applikation die GRASS-Software nicht mitgestartet wird. Bei der Verwendung von GRASS-Werkzeugen kommt es folglich zu einer Fehlermeldung. Dies lässt sich beheben, indem man die Anwendung _QGIS with GRASS_ (zu finden über die Suchfunktion des Computers) statt der Standardapplikation öffnet. 

## SAGA mit Linux
[SAGA ](http://www.saga-gis.org/en/index.html) ist eine weitere externe GIS-Software. SAGA-Werkzeuge sind durch ihr [Icon](https://4.bp.blogspot.com/-CBEWCwyOtag/UboZL1Zi8wI/AAAAAAAAEU8/FWczN9uFo-M/s1600/saga-logo.png) gekennzeichnet. Bei der Verwendung von  Windows oder MacOS als Betriebssystem wird SAGA bei der Installation von QGIS automatisch mitinstalliert. Bei Linux wird SAGA jedoch nicht automatisch mitinstalliert und muss manuell nachträglich installiert werden. Aus Erfahrung ist diese Installation aber nicht immer ganz leicht, sondern mit auftretenden Problemen verbunden. Alternativ kann man entweder eine Windows bzw. MacOS Virtualbox benutzen oder auf die Verwendung von SAGA-Werkzeugen verzichten (hierfür muss dann selbstständig nach alternativen Werkzeugen gesucht werden).

## Umlaute, Sonderzeichen, Leerzeichen in Dateipfaden 
Ein Dateipfad gibt den Ort auf einem Speichermedium an, an dem eine bestimmte Datei gespeichert ist. Sie werden im Rahmen jeder Task von eurem GIS Programm verwendet, um auf die Daten zugreifen zu können. Sollte QGIS den Dateipfad nicht lesen können, kann es auch mit den dort hinterlegten Dateien nicht interagieren und der Task schlägt fehl. Sollten in eurem Dateipfad Umlaute (ä,ö,ü), Sonderzeichen (!,?, ., etc.) oder Leerzeichen enthalten sein, kann dies zu Problemen bei der Bearbeitung dieser Dateien durch QGIS führen. Es ist daher zu empfehlen diese Zeichen in euren Dateipfaden zu vermeiden (Umlaute ausschreiben, Leerzeichen durch _ ersetzen).  
Folgende Dateipfade sind im Rahmen einer Taskbearbeitung durch QGIS entscheidend:

1) Eingabepfad (Input):  
Hier ist die Ursprungsdatei hinterlegt, auf deren Basis QGIS einen Task durchführen soll. Meistens handelt es sich um eine Layer-Datei, die zuvor in QGIS importiert wurde.

2) Ausgabepfad (Output):  
Hier wird die durch den Task entstehende Datei abgespeichert. Der Ausgabepfad wird von euch in den Werkzeugeinstellungen über die Funktion `Speichern unter ...` festgelegt. Damit GIS die Ausgabedatei auch wirklich in dem dafür vorgesehenen Ordner speichert, und ihr die Datei am Ende auch wiederfindet, ist es wichtig, diesen Speicherort vor dem Start eures Tools jedes Mal zu definieren. 

3) Temporäre Dateien:  
Während der Durchführung des Tasks muss QGIS Zwischenergebnisse erstellen. Diese werden in euren Temporären Dateien abgespeichert. Anders als die anderen beiden Dateipfade, ist dieser Pfad von eurem Betriebssystem festgelegt und sollte nicht verändert werden. Temporäre Dateien sind benutzerspezifisch (Wenn mehrere Personen einen PC verwenden, hat jede Person ihre eigenen temporären Dateien). Im Dateipfad befindet sich folglich euer Benutzername. Sollte dieser problematische Zeichen enthalten, kann es daher sinnvoll sein diesen abzuändern.  
Zu beachten gilt auch: Sollte man einen temporären Layer erzeugen, entspricht der Output (siehe 2) den temporären Dateien.

## Änderung von Einstellungen
Sollten Veränderungen an den Einstellungen von QGIS vorgenommen werden (wie z.B. [hier](home-Grundlegende Einstellungen) gezeigt), sind diese oft nach deren Bestätigung durch das Drücken der _OK_-Taste nicht sofort ersichtlich. Dies bedeutet jedoch nicht, dass die Änderungen nicht übernommen wurden. Stattdessen ist lediglich ein Neustart von QGIS nötig, um die Änderungen zu übernehmen (QGIS weist euch nicht darauf hin, dass ein Neustart benötigt wird).

## Versionsunterschiede  
Das Wiki und insbesondere die darin enthaltenen Videos sind immer nur eine Momentaufnahme. QGIS selbst, sowie auch die installierbaren Erweiterungen, werden durchgehend weiterentwickelt und verbessert. Zwischen den verschiedenen Versionen kann es somit zu Unterschieden in der Erscheinungsform der Benutzeroberfläche oder in seltenen Fällen sogar in der Funktion kommen. Folglich kann es zu Abweichungen zwischen dem Wiki und dem auf eurem PC installierten QGIS kommen.  

Solltet ihr Unterschiede zwischen dem Wiki und QGIS feststellen, könnt ihr gerne eure TutorInnen in den Übungsgruppen darüber informieren, sodass diese bei Bedarf das Wiki anpassen oder ergänzen können. 

## Videofunktionen 
Die Videos in diesem Wiki sind über ein Plugin des Browsers _Mozilla Firefox_ implementiert. [Auf dieser Website](https://support.mozilla.org/de/kb/html5-video-und-audio-firefox) im Abschnitt _Steuerelemente_ könnt ihr die verschiedenen Funktionen und Einstellungsmöglichkeiten für den Videoplayer nachlesen.  
 
**Hinweis:**  
Die Funktionalität des Videoplayers kann bei der Verwendung von anderen Browsern (Chrome, Edge, Safari, etc.) eingeschränkt sein. 