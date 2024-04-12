# Übung 2
## Ziel der Übung
* Nicht-räumliche Abfragen durchführen.
* Räumliche Abfragen durchführen.
* Geometrieoperationen nutzen (z.B. die Fläche eines Polygons berechnen).

## Wiki:
* [Nicht-Räumliche Abfragen](/content/gis/exercise_2/qgis-Nicht-Räumliche-Abfragen)
* [Räumliche Abfragen](/content/gis/exercise_2/qgis-Räumliche-Abfragen)
* [Geometrieoperationen](/content/gis/exercise_2/qgis-Geometrieoperationen)

## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_02/exercise_02_data.zip) und speichert sie auf eurem PC.
* World Administrative Boundaries Level 0 (Countries) (Polygon) (Quelle: [World Food Programme WFPGeonode](https://geonode.wfp.org/layers/geonode%3Awld_bnd_adm0_wfp))
* Urban Agglomerations Datensatz (Point) (Quelle: [UN World Urbanization Prospects 2018](https://population.un.org/wup/))

## Aufgaben

1. Öffnet die oben angegebenen Dateien im GIS.
2. Wählt 3 Städte eurer Wahl (manuell) in der Benutzeroberfläche aus. Öffnet nun die Attributtabelle und zeigt nur die Informationen für die ausgewählten Features an. Speichert die ausgewählten Features anschließend in einer neuen Datei (Layer).

    <details>
    <summary>Lösung</summary>
        <br/>
        <ul>
        <li>
        Manuelle Auswahlen werden immer auf dem Layer ausgeführt, den ihr gerade im Layerfenster ausgewählt habt.
        <li>
        Wenn ihr im Hauptfenster die Funktion "Objekte auswählen" (ungefähr mittig) anklickt, könnt ihr anschließend per Klick Objekte auswählen (mit Strg gedrückt halten, könnt ihr auch mehrere auswählen). Neben dem Button könnt ihr aus dem Dropdown-Menu auch auswählen, eine Auswahl per Polygon und ähnliches auswählen
        <li>
        In der Attributtabelle sinf ausgewählte Features blau hinterlegt. Unten links könnt ihr auswählen, welche Features ihr euch anzeigen lassen wollt. Wenn ihr dort "Gewählte Objekte anzeigen" auswählt, werden auch nur noch die ausgewählten Objekte angezeigt
        <li>
        Die ausgewählten Features könnt ihr mit einem Rechtsklick auf den Layer, Exportieren auswählen und dann "Gewählte Objekte speichern" speichern.
        </ul>
        <br/><br/>

    </details>

<br>

3. In welcher Einheit liegen die Einwohnerzahlen vor? Dies ist für die folgenden Aufgaben wichtig.

    <details>
    <summary>Lösung</summary>
        <br/>
        <ul>
        <li>
        1000 Einwohner
        </ul>
        <br/><br/>

    </details>
<br>

4. Wählt nun anhand einer Abfrage (automatisch) alle Städte, welche im Jahr 2015 mehr als 15 Millionen Einwohner hatten. Wie viele Städte gibt es, die diese Bedingung erfüllen? Welche Stadt hat die meisten Einwohner?

    <details>
    <summary>Lösung</summary>
        <br/>
        <ul>
        <li>
        Öffnet die Attributtabelle und wählt "Select features by an expression" aus.
        <li>
        Gebt dort den Ausdruck '"2015" > 15000' ein und führt die Selektion aus.
        <li>
        Ganz oben in der Attributtabelle wird euch angezeigt, wie viele Features ausgewählt sind. Mit einem Klick auf den Spaltennamen wird die Spalte sortiert. Wenn ihr sie auf absteigend stellt, könnt ihr sehen, welche Stadt die höchste Einwohnerzahl aufweist.
        </ul>
        <br/><br/>

    </details>
<br>

5. Führt nun eine kombinierte Selektion durch. Selektiert zunächst alle Städte in China. Entfernt anschließend alle Städten mit einer Einwohnerzahl kleiner als 1 Million aus dieser Auswahl. Wie viele Millionenstädte gibt es in China?

    <details>
    <summary>Lösung</summary>
        <br/>
        <ul>
        <li>
        Öffnet die Attributtabelle und wählt "Select features by an expression" aus.
        <li>
        Gebt dort den Ausdruck '"Country or" Like 'China' AND  "population" < 1000' ein.
        <li>
        In den Attributtabelle aktviert nun den Bearbeitungsmodus entweder auf dem Button ganz links oder mit Strg+E.
        <li>
        Klickt nun auf den Button "Delete selected features"
        </ul>
        <br/><br/>

    </details>

6. Berechnet die Fläche jedes einzelnen Features in Quadratmeter. (Bei Fragestellungen dieses Typs ist es besonders wichtig die Projektion der Daten zu beachten. Wir nutzen hier hier Mollweide (EPSG: 54009), eine flächentreue Projektion.) Welches ist das kleinste Land der Welt und wie groß (klein) ist es? Unter Land verstehen wir hier alle Features mit dem Status *Member State*.

    <details>
    <summary>Lösung</summary>
        <br/>
        <ul>
        <li>
        Öffnet die Attributtabelle und wählt den Feldrechner aus.
        <li>
        Gebt dem neuen Feld einen Namen und wählt als `Output field type` "Whole number (integer 64 bit) aus.
        <li>
        Gebt als Ausdruck '$area' ein und erstellt das neue Feld.
        </ul>
        <br/><br/>

    </details>
<br>
