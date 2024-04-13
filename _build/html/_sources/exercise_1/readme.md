# Exercise 01

## Ziel der Übung
* (1) Datenorganisation (GitLab und eigene Strukturierung) + GIS-Programm einrichten
* (2) Erste Schritte mit Layern + Kartengestaltung

## Wiki
* [Installation](/content/gis/allgemeines/qgis-Installation.md)
* [Hinweise zur Verwendung von GIS-Software](/content/gis/allgemeines/Hinweise.md)
* [Was tun bei Problemen?](/content/gis/allgemeines/home-Probleme.md)
* [Grundlegende Einstellungen](/content/gis/exercise_1/arbeiten_mit_qgis/home-Grundlegende_Einstellungen.md)
* [Benutzeroberfläche anpassen](/content/gis/exercise_1/arbeiten_mit_qgis/qgis_Interface.md)
* [Datenorganisation](/content/gis/exercise_1/arbeiten_mit_qgis/home-Datenorganisation.md)
* [Geodatenformate](/content/gis/exercise_1/arbeiten_mit_qgis/home-Geodatenformate)
* [Layer-Konzept kennenlernen](/content/gis/exercise_1/daten_in_qgis/qgis-Layer-Konzept.md)
* [Interface](/content/gis/exercise_1/arbeiten_mit_qgis/qgis-Interface.md)
* [Attributdaten](/content/gis/exercise_1/daten_in_qgis/qgis-Attributdaten)
* [Projektionen](/content/gis/exercise_1/daten_in_qgis/qgis-Projektionen)
* [Vektorsignaturen](/content/gis/exercise_1/visualisierung/qgis-Vektorsignaturen)
* [Kartengestaltung](/content/gis/exercise_1/visualisierung/qgis-Kartengestaltung)

## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_01/exercise_01_data.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)

* Punkt-Layer: Next-Bike Ausleihpunkte (Quelle: [OpenStreetMap and Contributors](https://www.openstreetmap.org/#map=6/51.330/10.453))
* Linien: Neckar (Quelle: [OpenStreetMap and Contributors](https://www.openstreetmap.org/#map=6/51.330/10.453))
* Polygon-Layer (Quelle: [OpenStreetMap and Contributors](https://www.openstreetmap.org/#map=6/51.330/10.453)):
  * Einzugsgebiete der Next-Bike Stationen (gibt an wie lange man zu Fuß zur nächsten Station benötigt)
  * Grenze Heidelbergs
  * Stadtteilgrenzen

## Aufgabenteil 1 - Programme und Datenorganisation
1. Verschafft euch einen Überblick über GitLab. Seht euch die Seiten ***Repository***, in dem alle Übungen und Abgaben, sowie ein zeitlicher Übersichtsplan über den Verlauf des Tutoriums zu finden sind.

2. Verschafft euch einen Überblick über die beste Vorgehensweise bei [Problemen](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/home-Probleme), die in der Arbeit mit GIS auftreten können: ***Wiki*** (in dem Informationen und Erklärvideos zu allen behandelten Themenbereichen gesammelt sind), und ***Issues*** (in denen Fragen gestellt und Probleme besprochen werden können)

3. Macht euch mit dem Thema [Datenorganisation](/content/gis/exercise_1/arbeiten_mit_qgis/home-Datenorganisation) vertraut und erstellt eine geeigntete Ordnerstruktur, mit der ihr im kommenden Semester arbeiten könnt.

4. Informiert euch über verschiedene [Geodatenformate](/content/gis/exercise_1/arbeiten_mit_qgis/home-Geodatenformate).

5. Entscheidet euch für ein GIS-Programm (***ArcGIS*** oder ***QGIS*** – Was sind Vor- und Nachteile der beiden Programme?) und beginnt den Download-Prozess unter Beachtung der Hinweise zur [Installation](/content/gis/allgemeines/qgis-Installation).
   Hinweis zu den Programmen: das Wiki zu QGIS ist sehr viel ausführlicher und aktueller, zudem können euch nicht alle Tutor*innen bei Problemen in ArcGIS unterstützten. Als Anfänger*innen ist die Nutzung von QGIS zu empfehlen.

6. Öffnet euer GIS und nehmt erste [Einstellungen](/content/gis/exercise_1/arbeiten_mit_qgis/home-Grundlegende-Einstellungen) in eurem GIS nach den Empfehlungen im Wiki vor (ändert zum Beispiel die Sprache).

## Aufgabenteil 2 - Verständnis und Nutzung von GIS-Programmen
1. Öffnet die oben angegebenen Dateien im GIS. Ladet dazu die Vektor-Layer in euer Programm.

2. Interagiert mit der Karte und erkundet die Datensätze. Verwendet hierfür das Zoom-Werkzeug und verschiebt die Karte. Beachtet dabei die Statusleiste am unteren Bildschirmrand und wie diese sich verändert. Wie lauten die ungefähren Koordinaten für die westlichste Nextbike-Station?

3. Macht eucht mit dem Layer-Fenster (Layer List) vertraut. Blendet abwechselnd verschiedene Layer ein und aus und verschiebt die Layer in der Hierarchie. Benennt eine Layer um und beachtet, dass dies keine Auswirkung auf die Datenquellen (Dateinamen, Speicherort) hat.

4. Seht die Attributdaten der Layer ein. Schaut euch zu diesem Zweck die Attributtabelle an und macht euch mit der zugehörigen Nutzeroberfläche vertraut. Wie viele Features gibt es im Layer stadtteile? Wie viel Kapazität hat die Nextbike-Station am Hans-Thoma-Platz?

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Rechtsklick auf den Layernamen und Attributtabelle öffnen auswählen.


  </details>

5. Ändert die Projektion in der Kartenansicht zu WGS84 UTM32N (EPSG-Code: 32632). ***Beachtet, dass dies nichts an der Projektion (den Koordinaten) der Dateien ändert, sondern lediglich die Projektion der Kartenansicht beeinflusst.*** Überprüft dies in den Eigenschaften des Punkt-Layers. Welche Projektion ist dort angegeben?

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Die Angabe zur Projektion (KBS) findet ihr unter Eigenschaften -> Informationen. Eine Vekotrlayer kann reprojiziert werden unter Vektor -> Datenmanagment-Werkzeuge -> Layer reprojizieren.


  </details>

6. Nachdem ihr euch mit dem Programm vertraut gemacht habt, geht es jetzt über zur spezifischeren Anwendung und Kartengestaltung. Denkt daran euer Projekt zu speichern.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Speichert euer Projekt unter Projekt -> Speichern als... . Die Projektdatei (.qgz) speichert nicht alle eure Daten, löscht also nicht eure einzelnen Layerdateien, da das Projekt auf diese zugreift.

  </details>

7. Wählt für das Punkt-Layer, sowie Linien-Layer passende [Signaturen](/content/gis/exercise_1/visualisierung/qgis-Vektorsignaturen)

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Im verlinkten Wiki findet ihr hierzu kurze Screenrecordings, welche die verschiedenen Gestaltungsmöglichkeiten erklären. Tipp: Unter Ansicht -> Bedienfelder -> Layergestaltung kann man sich das Feld anzeigen lassen ohne ein neues Fenster zu öffnen.


  </details>

8. Nutzt für die Darstellung der Einzugsgebiete eine abgestufte Farbskala.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Wählt die Layer isochronen aus und wählt im Bedienfeld Layergestaltung die Einstellung Abgestuft anstatt Einzelsymbold aus. Legt nun den Wert fest (hier: AA_MINS), sucht einen Farbverlauf aus und klickt auf Klassifizieren.


  </details>

9. Beschriftet die Stadtteile mit ihrem Namen.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Layergestaltung -> Beschriftung (Pfeilsymbol "abc") wählen und von keine Beschriftung auf Einzelne Beschriftung umstellen und auch hier den Wert (hier: name) festlegen.


  </details>

10. Ändert das Koordinatenbezugssystem (Projektion) eurer Ansicht auf ein für Deutschland passenderes.

11. Erstellt eine neue Druckzusammenstellung. Nutzt das Format A4 (Querformat) für eure Karte([siehe hier](/content/gis/exercise_1/visualisierung/qgis-Kartengestaltung))

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Wie ihr ein Kartenblatt erstellen könnt findet ihr ausführlich im Wiki erklärt. Mit einem Rechtsklick auf das Kartenblatt könnt ihr die Seiteneigenschaften öffnen und das Format abändern.

  </details>

12. Stellt einen passenden Maßstab ein (z.B. 1:75000).

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Nachdem ihr die Karte zum Layout hinzugefügt habt könnt ihr unter Elementeigenschaften den Maßstab der Karte festlegen.


  </details>

13. Verseht eure Karte mit Nordpfeil und Maßstab (Maßstabsbalken und Numerischen Maßstab).

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Die nötigen Tools finden sich in der vertikalen Symbolleiste am linken Rand des Feldes.


  </details>

14. Fügt abschließend Legende, Kartentitel, Autor und Datenquelle hinzu.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Die nötigen Tools finden sich in der vertikalen Symbolleiste am linken Rand des Feldes. Schriftart, -größe, Rand oder Hintergrund können unter Elementeigenschaften angepasst werden.


  </details>

15. Speichert eure Karte als PDF.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Layout -> als PDF exportieren.  


  </details>
