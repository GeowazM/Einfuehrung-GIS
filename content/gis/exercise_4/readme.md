# Übung 4
## Ziel der Übung
* web-basierte Hintergrundkarten nutzen
* Vektordaten händisch erstellen (Digitalisieren)
* Ein Bild Georeferenzieren


## Wiki:
* [Basemaps](/exercise_4/qgis-Basemaps)
* [Digitalisieren](/exercise_4/qgis-Digitalisierung)
* [Georeferenzieren](/exercise_4/qgis-Georeferenzierung)


## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_04/exercise_04_data.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)


## Aufgaben
### Häuser und Straßen kartieren

1. Erstellt zwei neue Layer für (a) Häuser und (b) Straßen in Heidelberg.
<details>
  <summary>Lösung</summary>
    (a) Layer > Create Layer > new Shapefile Layer: Namen + Dateipfad angeben, Geometry type: Polygon, metrische Projektion auswählen
    XXX
    <li>
     (b) Layer > Create Layer > new Shapefile Layer: Namen + Dateipfad angeben, Geometry type: Line, metrische Projektion auswählen
     </ul>
    <br/><br/>

  </details>
2. Fügt zu jedem Layer ein Attribute "Name" hinzu.
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Attributtabelle öffnen, in Bearbeitungsmodus umschalten (Str+E), Neue Spalte (Str+W): Name: Name, Typ: Text (string)
    <br/><br/>

  </details>
3. Nutzt als Kartierungsgrundlage eine Hintergrundkarte auf Basis von Satellitendaten (z.B. Bing)
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Web > QuickMapServices > SearchQMS: Bing Aerial auswählen
    <br/><br/>

  </details>
4. Erstellt mindestens 3 Gebäude und 3 Straßen im Heidelberger Stadtgebiet. Erstellt mindestens 1 Gebäude mit einem Innenhof (z.B. Mathematikon).
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Layer auswählen, falls nicht in Bearbeitungsmodus: Bearbeitungsstatus umschalten, Polygonobjekt hinzufügen (Str+.), dann Eckpunkte setzen; Rechtsklick schließt Vorgang ab
    <li>
     analog für Straßen, dort muss allerdings anstatt von "Polygonobjekt hinzufügen" "Linienobjekt hinzufügen" ausgewählt werden
     </ul>
    <br/><br/>

  </details>
5. Fügt zu jedem Feature den passenden Namen hinzu.
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Nach dem rechtsklick bei Musterlösung von 4. beim Feld "Namen", welches in Schritt 2 hinzugefügt wurde, den Namen vom jeweiligen Objekt eingeben
    <br/><br/>

  </details>


### Ein Bild georeferenzieren
#### Kontext
Das Kurpfälzische Museum möchte historische Daten aus Heidelberg mit einer Hintergrundkarte versehen. Hierfür benötigt das Museum eine geeignete georeferenzierte Karte. Ihr sollt die folgende historische Karte von 1821 georeferenzieren:

![Heidelberg_1821](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_04/Heidelberg_1821.jpg)

**Hinweis: in einigen QGIS-Versionen lässt sich das Georeferenzierungs-Tool auch unter "Layer" finden!**

1. Verseht das zur Verfügung gestellte Raster mit WGS84 Pseudo-Mercator-Koordinaten (EPSG: 3857).
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Raster > Georeferenzierung: zu georeferenzierenden Geodatensatz öffnen und Projektion auswählen
    <br/><br/>

  </details>
2. Verwendet als Referenz-Layer Webkarten eurer Wahl, welche ihr in Form einer Hintergrundkarte einbinden könnt.
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Siehe Digitalisierung Schritt 3: Bing Aerial
    <li>
    alternativ: Web > QuickMapServices > OSM > OSM Standard
     </ul>
    <br/><br/>

  </details>
3. Wählt eine geeignete Transformationsvorschrift und setzt genügend und ausreichend verteilte Passpunkte.
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Siehe Wiki: Auswahl des Transformationstyps je nach Größe, Verzerrung, etc. des Ausschnitts. Im konkreten Beispiel: Polynomial 1, da kleiner, wenig verzerrter Ausschnitt. Resampling Methode: Nächster Nachbar, Projektion: siehe 1. Es sind theoretisch mindestens 4 Punkte zu setzen, allerdings bietet es sich an, mehr als 8 Punkte zu setzen, dass das Bild genauer zu verorten ist.
    <br/><br/>

  </details>
4. Kontrolliert abschließend euren Erfolg, indem ihr die Passgenauigkeit des georeferenzierten Bildes mit überlagerten Hintergrundkarte vergleicht.
<details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Wichtiger Hinweis: es handelt sich bei der historischen Darstellung Heidelbergs NICHT im eine Karte, sondern um eine Kartenähnliche Darstellung. Aufgrund mangelnder Genauigkeit kann keine präzise Georeferenzierung vorgenommen werden.
    <br/><br/>

  </details>
