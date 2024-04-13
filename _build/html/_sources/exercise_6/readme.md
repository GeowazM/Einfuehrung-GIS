# Übung 6
## Ziel der Übung
* Rasterdaten im GIS öffnen und kennenlernen
* farbliche Darstellung der Rasterwerte anpassen
* Rasterdaten in Vektordaten umwandeln
* Globale Rasteroperationen anwenden (z.B. Projektion ändern)
* Lokale Rasteroperationen anwenden (z.B. NDVI berechnen)

## Wiki:
* [Rasterdaten im GIS öffnen und kennenlernen](/content/gis/exercise_6/qgis-Layer-Konzept)
* [Darstellung von Rasterdaten](/content/gis/exercise_6/qgis-Rasterdarstellung)
* [Vektordaten in Rasterdaten umwandeln](/content/gis/exercise_6/qgis-Konvertierung)
* [Globale Rasteroperationen](/content/gis/exercise_6/qgis-Globale-Funktionen)
* [Lokale Rasteroperationen](/content/gis/exercise_6/qgis-Lokale-Funktionen)

## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_06/exercise_06_data.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)

## Aufgaben
### Aufgabe 1: Vorbereitung
* Erstellt zunächst ein Mosaik aus den einzelnen Dateien des ASTER-Höhenmodells.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Wählt die Funktion <b>Merge</b> aus und gebt die vier Aster-Raster dort als <i>Input</i> ein.

     </ul>
    <br/><br/>

  </details>

* Bringt anschließend das Aster-Höhenmodell in eine metrische Projektion.


  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Warp (reproject)</b> mit z.B. EPSG:32636 - WGS 84 / UTM zone 36N anwenden.

     </ul>
    <br/><br/>

  </details>


### Aufgabe 2: Arbeiten mit Geländemodellen
* Verschafft euch einen Überblick über die Höhenwerte. Was sind die maximalen und minimalen Höhen im Untersuchungsgebiet. Schaut dies in den Layer-Eigenschaften nach.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Die Höhenwerte können entweder im Layers-Fenster direkt unter dem Layernamen gesehen werden, ansonsten kann mit Rechtsklick auf den Layer -> Properties -> Information und dann unter <i>Bands</i> der Min- und Max-Wert eingesehen werden. Es kann auch die Funktion <b>raster layer statistics</b> genutzt werden.

     </ul>
    <br/><br/>

  </details>

* Reklassifiziert das Aster-Höhenmodell in 500 Meter Schritten.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Reclassify by table</b> auf den reprojezierten Layer anwenden. In die Tabelle zehn Spalten einfügen nach diesem Muster: <br>
    |0|500|1<br>
    |500|1000|2 <br>
    |1000|1500|3<br>
    ...

     </ul>
    <br/><br/>

  </details>

* Erstellt nun Höhenlinien (Konturlinien) und exportiert diese im Vektorformat.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Contour</b> auswählen. Bei <i>Interval between contour lines</i> 1 eingeben.

     </ul>
    <br/><br/>

  </details>


### Aufgabe 3: Arbeiten mit Landsat-Daten
* In dieser Aufgabe arbeiten wir mit Daten der Landsat 8 Mission. Wir nutzen nur die Bänder 2-5 in unserer Analyse. Welchen Farben entsprechen diese Bänder?

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Nachschauen auf der offiziellen Seite der NASA (https://landsat.gsfc.nasa.gov/satellites/landsat-8/landsat-8-bands/) zeigt: Band 2 = Blau, Band 3 = Grün, Band 4 = Rot, Band 5 = Nahes Infrarot.

     </ul>
    <br/><br/>

  </details>

* Erstellt ein Raster Komposit (bzw. Virtual Raster) aus den gegebenen Bändern.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Build virtual raster</b> auswählen. Die Landsat-Layer als <i>Input layers</i> wählen und bei <i>Resolution</i> Highest wählen. Haken setzen bei <i>Place each input file into a seperate layer</i>.

     </ul>
    <br/><br/>

  </details>

* Visualisiert das Komposit in Falschfarben, sodass Vegetation rot erscheint.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Rechtsklick auf den virtuellen Raster -> Properties -> Symbology
    <li>
    Bei <i>Render type</i> Multiband color auswählen und anschließend für <i>Red band</i> Near Infrared (Band 4), für <i>Green band</i> Red (Band 3) und für <i>Blue band</i> Green (Band 2) auswählen.

     </ul>
    <br/><br/>

  </details>

* Berechnet den Normalized Difference Vegetation Index.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Formel: NDVI = (NIR - Rot) / (NIR + Rot) für dieses Raster bedeutet das NDVI = (Band 4 - Band 3) / (Band 4 + Band 3)
    <li>
    Öffne den <b>Raster Calculator</b> und gib folgende Formel ein:  '( "Virtual@4" - "Virtual@3" )  /  ( "Virtual@4" + "Virtual@3" )'.

     </ul>
    <br/><br/>

  </details>

* Erstellt anschließend NDVI-Klassen. Orientiert euch dabei an folgender Einteilung.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Nutze die Funktion <b>Reclassify by table</b> und gebt als die <i>Reclassification table</i> folgende Spalten ein: <br>
    |-1|0|1|<br>
    |0|0.2|2|<br>
    |0.2|0.4|3|<br>
    |0.4|1|4|

     </ul>
    <br/><br/>

  </details>

* Stellt die Klassen farblich sinnvoll dar.

| Kategorie | NDVI |
| --- | --- |
|Wasser und Schnee| < 0 |
| Felsen, Sand, Gebäude | 0 - 0.2 |
| Gras, Sträucher | 0.2 - 0.4 |
| Wald und intensive Landwirtschaft | >0.4 |
