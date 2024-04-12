# Übung 3
## Ziel der Übung
* Geometriefunktionen vertiefen.
* Vektordaten räumlich Verschneiden.
* Räumliche Joins durchführen.
* Tabellenfunktionen nutzen und einfache Statistiken erstellen.

## Wiki:
* [Geometrieoperationen](/content/gis/exercise_3/qgis-Geometrieoperationen)
* [Räumliche Verschneidungen](/content/gis/exercise_3/qgis-Räumliche-Verschneidungen)
* [Räumliche Joins](/content/gis/exercise_3/qgis-Räumliche-Joins)
* [Tabellenfunktionen](/content/gis/exercise_3/qgis-Tabellenfunktionen)

## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_03/exercise_03_data.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)

* Osnabrück Fluss Hase (Line) (Quelle: [OpenStreetMap](https://www.openstreetmap.org))
* Osnabrück Straßennetzwerk (Line) (Quelle: [OpenStreetMap](https://www.openstreetmap.org))
* Osnabrück Stadtgrenze (Polygon) (Quelle: [OpenStreetMap](https://www.openstreetmap.org))
* Osnabrück Gebäude (Polygon) (Quelle: [OpenStreetMap](https://www.openstreetmap.org))

## Aufgaben

### Datenvorbereitung
1. Schneidet den Gebäude-Datensatz und den Straßen-Layer auf das Stadtgebiet Osnabrücks zu (Clip).

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Wähle Vektor >> Geoverarbeitungswerkzeuge >> Zuschneiden... die Eingabelayer ist die Layer die du kleiner schneiden möchtest, für Layer überlagern wähle osnabrueck_admin. Die zugeschnittene Layer wird als neue Layer erscheinen, vergesse nicht diese umzubenennen um Verwirrung zu vermeiden. Wiederhole den Prozess bis alle Layer auf das gleiche Maß zugeschnitten sind.


  </details>

2. Projiziert anschließend alle Daten in ein metrisches Koordinatensystem.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Reprojiziere die einzelnen Layer unter Layer >> Layer reprojizieren und wähle die gewünschte Projektion aus. Auch hier wird eine neue Layer erstellt die du umbennenen solltest. Außerdem handelt es sich um eine Temporärlayer, mache diese permanent.

  </details>

### Hochwasserbereich ermitteln
3. Verbindet alle Teilstücke der Hase zu einer einzelnen Geometrie. Nutzt dazu die Dissolve-Funktion.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Verwende das Tool Auflösen (unter Vektorgeometrie).

  </details>

4. Zur Berechnung der Hochwassergefahr nutzen wir einen vereinfachten Ansatz. Berechnet 3 Stufen der Hochwassergefahr mithilfe der (Multiple)Buffer-Funktion:
  (a) alle Bereiche in Abstand von maximal 100 m zur Hase,
  (b) alle Bereiche zwischen 100 m und 200 m Abstand,
  (c) alle Bereiche mit einem Abstand von mehr als 200 m bis zu 300 m.
* optional: Färbt die Bereiche ensprechend der Hochwassergefahr ein.

<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Verwende das Vektor-Tool Mehrringpuffer, wähle die Layer osnabrueck_hase als Eingabelayer und stelle die Ringanzahl auf drei und den Abstand auf 100 m. Die Farben der neuen Layer kannst du ganz normal unter Layergestaltung umstellen.

  </details>


### Gebäude nach Hochwassergefahr einteilen
5. Fügt zu jedem Gebäude die maximale Hochwassergefahrenklasse (a, b, c) hinzu. Nutzt dafür die Spatial-Join Funktion.


<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Verwende Attribute nach Position zusammenfügen. Die Eingabelayer ist osnabrueck_buildings und die neue Bufferlayer für Layerverknüpfen. Für diese Aufgabe möchtest du innerhalb wählen.

  </details>

6. Zählt wie viele Gebäude in jede der drei Klassen vorhanden sind. Erstellt dazu eine kategorisierte Statistik der Attributwerte in Form einer Tabelle und speichert diese.
* optional: Färbt die Gebäude ensprechend der Hochwassergefahr ein.
* optional: Visualisiert die Statistik mit einem Balkendiagramm. Nutzt dafür ein Programm eurer Wahl (z.B. Excel).


<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Öffne Statistik nach Kategorien, wähle die Eingabelayer ud das Feld für die Statistikberechnung aus.  

  </details>


### Hochwassergefährdete Bereiche im Straßennetzwerk ausweisen
7. Verschneidet das Straßennetzwerk mit dem Hochwassergefahr-Layer.


<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Genau wie das Tool Zuschneiden vom Beginn der Exercise gibt es auch die Einstellung Verschneidung.

  </details>

8. Berechnet anschließend die Länge der neu enstandenen Straßensegmente.
9. Auf welcher Gesamtlänge sind die unterschiedlichen Straßentypen möglicherweise von Hochwasser pro Klasse (a, b, c) betroffen? Erstellt dafür eine gruppierte Statistik.
* optional: Visualisiert die Statistik in einem Balkendiagramm. Nutzt dafür ein Programm eurer Wahl (z.B. Excel).


## So (oder ähnlich) sieht's am Ende aus

![osnabrueck_karte](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_03/osnabrueck_karte.png)

![building_stats](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_03/building_count_stats.png)

![road_stats](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_03/road_length_stats.png)
