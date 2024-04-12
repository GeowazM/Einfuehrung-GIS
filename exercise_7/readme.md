# Übung 7
## Ziel der Übung
* Rasterdaten zuschneiden  
* Reliefanalysen durchführen
* zonale Statistiken berechnen
* Rasterdaten in Vektordaten umwandeln
* ein Höhenprofil erstellen

## Wiki:
* [Rasterdaten in Vektordaten umwandeln](/exercise_7/qgis-Konvertierung)
* [fokale Rasteroperationen](/exercise_7/qgis-Fokale-Funktionen)
* [zonale Rasteroperationen](/exercise_7/qgis-Zonale-Funktionen)
* [weitere Rasteroperationen](/exercise_7/qgis-Weitere-Rasterfunktionen)

## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_07/exercise_07_data.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)
* Polygon-Layer: national_parks (Quelle: OpenStreetMap and Contributors)
* Linien-Layer: trails (Quelle: OpenRouteService, OpenStreetMap and Contributors)
* Raster-Layer: ASTER Höhendaten (Quelle: METI/NASA)

## Aufgaben
### Aufgabe 1: Vorbereitung
* Bringt die Höhendaten in eine passende metrische Projektion (z.B. UTM37N).

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    `ASTER_merged.tiff` -> Funktion <b>Warp (Reproject)</b>, Ziel-KBS "EPSG: 32637 - WGS 84 / UTM zone 37N"
    -> speichern als z.B. `ASTER_reprojected`
     </ul>
    <br/><br/>

  </details>

* Schneidet den Raster-Datensatz auf die Ausdehnung des Nationalpark-Layers zu.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Clip Raster by Extent</b>, Inputlayer `ASTER_reprojected`, Clipping Extent -> Calculate from Layer -> `national_parks` -> speichern als z.B. `ASTER_clipped`
     </ul>
    <br/><br/>

  </details>


### Aufgabe 2: Reliefanalysen
* Berechnet zunächst einen Hillshade für das Geländemodell.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Hillshade</b>, Input Layer `ASTER_clipped`
    -> speichern als z.B. `hillshade`
     </ul>
    <br/><br/>

  </details>

* Ermittelt die Steigung in °.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Slope</b>, Input Layer `ASTER_clipped`
    -> speichern als z.B. `slope`
     </ul>
    <br/><br/>

  </details>

* Erstellt Übersichtsstatistiken für die beiden Nationalparks.
  * Was ist die maximale Steigung pro Nationalpark?
  * Wie hoch ist die durchschnittliche Steigung pro Nationalpark?

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Zonal statistics</b>, Input Layer `national_parks`, Raster Layer `slope`, Statistics to calculate "Mean" und "Maximum"
    -> speichern als z.B. `zonal_statistics`
    <li>
    Ergebnisse können in der Attributtabelle eingesehen werden
     </ul>
    <br/><br/>

  </details>

* Glättet euer Ergebnis in dem ihr pro Pixel den Durchschnitt der 11x11 Nachbarschaft berechnet.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>r.neighbors</b>, Input raster layer `slope`, Neighborhood operation "average", neighborrhood size "11"
    -> speichern als z.B. `smoothed`
     </ul>
    <br/><br/>

  </details>

* Selektiert besonders steile Regionen (>30°) (nutzt dazu zunächst den Raster Calculator oder das Reclassify Tool)

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Raster Calculator mit Befehl '"smoothed@1" > 30' -> speichern als z.B. `calculated`
     </ul>
    <br/><br/>

  </details>

* Konvertiert die Auswahl ins Vektorformat.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Funktion <b>Polygonize (Raster to Vector)</b>, Input Layer `calculated`
     </ul>
    <br/><br/>

  </details>

### Aufgabe 3: Höhenprofil
* erstellt für die Sirimon-Route im trails-Layer ein Höhenprofil.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Installiert das Plugin "Profile tool". Anschließend könnt ihr das über Plugins -> Profile Tool öffnen. Im Layerfenster den Layer `ASTER_reprojected` auswählen und im Profile Tool <i>Add Layer</i> auswählen- Bei Options Selection auf <i>Selected Layer</i>stellen. Anschließend den  Layer `trails` auswählen-
     </ul>
    <br/><br/>

  </details>

* Das Höhenprofil soll auf der x-Achse die Distanz in Meter zeigen, auf der y-Achse die Höhe ü.N.

Das könnte dann ungefähr so aussehen:
![profile](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_07/sirimon_route_profile.png)
