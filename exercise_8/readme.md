# Übung 8
## Ziel der Übung
* Räumliche Interpolation anwenden
* Rasterfunktionen vertiefen

## Wiki:
* [Räumliche Interpolationsverfahren](/exercise_8/qgis-Räumliche-Interpolationsverfahren)
* [lokale Rasterfunktionen](/exercise_6/qgis-Konvertierung)


## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_08/exercise_08_data.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)
* Höhenmodell: germany_dem.tif (Quelle: [GTOPO30 USGS](https://www.usgs.gov/centers/eros/science/usgs-eros-archive-digital-elevation-global-30-arc-second-elevation-gtopo30?qt-science_center_objects=0#qt-science_center_objects))
* Messstationen: temp_stations.shp
* Durchschnittstemperaturen für den Zeitraum 1960-1990: mean_temp.csv

## Aufgaben
### Aufgabe 1: Vorbereitung
* Bringt die Daten in ein geeignetes Koordinatensystem.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    `germany_dem` -> Funktion <b>Warp (Reproject)</b>, Ziel-KBS "EPSG: 32632 - WGS 84 / UTM zone 32N"
    <li>
     `temp_stations` -> Funktion "Reproject layer", Ziel-KBS "EPSG: 32632 - WGS 84 / UTM zone 32N"
     </ul>
    <br/><br/>

  </details>

* Selektiert nur Stationen mit einer gültigen Höhenangabe.
  <details>
  <summary>Lösung</summary>
  <br/>
    <ul>
      <li>
      Untersuche Attributtabelle des `temp_stations`-Layers; Höhenangabe in der "ELEV"-Spalte -> NoData-Value ist -999 (Wert in Deutschland nicht möglich).
      <li> Entfernen der Stationen mit dieser Höhenangabe, z.B. über <i>Select features using an expression</i> in der Attributtabelle oder Funktion <b>Select by expression</b>
    jeweils mit Ausdruck '"ELEV" = -999'. Anschließend den Layer mit <i>Toggle Editing</i> in den Bearbeitungsmodus bringen und dann <i>delete selected layers</i>. Alternativ
    kann auch die Filterfunktion des Layers genutzt werden mit Rechtsklick auf den Layer -> Filter -> Ausdruck '"ELEV" != -999'.
    </ul>
    <br/><br/>

  </details>

* Fügt die durchschnittliche Jahrestemperatur als Attribut der Messstationen hinzu. Nutzt dazu einen Join.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Übereinstimmende Felder: "TEMP_STA_1" von `temp_stations` und "STATION_ID" von `mean_temp`. Allerdings ist "TEMP_STA_1" als Zahl (Integer) und "STATION_ID" als Text (String) abgespeichert.
    Mögliche Lösung: Erstelle ein neues Feld in z.B. dem `temp_stations`-Layer mit der Funktion <b>Field calculator</b>. Dort als result field type "Text (string)" auswählen
    und als Ausdruck nur '"TEMP_STA_1"' eingeben (Name des neuen Feldes z.B. "ID").
    <li>
    Funktion <b>Join attributes by field value</b>, Inputlayer `temp_stations`
    Table field "ID", Inputlayer 2 `mean_temp` Table field "STATION_ID", optional bei <i>Layer 2 fields to copy</i> die Spalte "YEAR" auswählen, da es die einzige ist, die wir weiterhin brauchen
     </ul>
    <br/><br/>

  </details>

### Aufgabe 2: Temperaturwerte anpassen und Interpolation durchführen.
* Berechnet für jede Messstation eine normalisierte Jahresdurchschnittstemperatur. Diese soll die Temperatur angeben, wenn die Messstation auf 0 m üNN liegen würde. Nutzt dafür folgenden Zusammenhang:
  * Temperaturabnahme um 0,54°C je 100 Höhenmeter

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Beachte, dass die "YEAR"-Spalte im Textformat vorliegt und nicht für die Interpolationgenutzt werden kann bevor der Datentyp geändert wurde.
    <li>
    Da für diese Aufgabe sowieso noch eine Umrechnung stattfindet, bei der der Datentyp automatisch angepasst werden kann, ist das nicht unbedingt nötig. Falls doch gwünscht,
    kann hierfür wieder die Funktion <b>field calculator</b> genutzt werden. Das result field sollte diesmal "decimal number (real)" genutzt werden und als Ausdruck nur "YEAR".
    Ansonsten erfolgt die Normalisierung der Temperaturwerte auch über den "field calculator" mit dem Ausdruck '"YEAR" + ("ELEV" / 100 * 0.54)'.

     </ul>
    <br/><br/>

  </details>

* Inpterpoliert anhand der gewonnenen Werte die Durchschnittstemperaturen in Deutschland.
  * Nutzt dazu Inverse Distanz Gewichtung (IDW)
  * und einen Power-Wert von 2

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Für die Interpolation sollte die Funktion <b>IDW Interpolation</b> genutzt werden. Hier den bearbeiteten "temp_stations"-Layer als Inputlayer und als <i>Interpolation attribute</i>
    das zuvor berechnete Feld mit der normalisierten Temperatur. Anschließendauf das grüne Plus drücken. Beim Extent rechts <i>calculate from layer</i> auswählen
    und den bearbeiteten "temp_stations"-Layer nutzen. Anschließend muss noch die <i>Pixel size X</i> angepasst werden (<i>Pixel size Y</i>) wird automatisch mit angepasst.
    Wir empfehlen eine <i>pixel size X</i> von 1000 (in diesem Fall Metern).

     </ul>
    <br/><br/>

  </details>

* Korrigiert eure gewonnenen Ergebnisse erneut unter Berücksichtigung der tatsächlichen Höhe. Nutzt dazu den Raster-Calculator und den oben genannten Zusammenhang und das Höhenmodell.

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Nach der Ausführung der Interpolation muss nun wieder die Höheninformation in das Ergebnis einfließen. Dafür wird der <b>Raster-Calculator</b> genutzt.
    Folgender Ausruck sollte genutzt werden: '"Interpolated@1" -  ( "germany_dem_eprojected@1"/100 * 0.54)'.

     </ul>
    <br/><br/>

  </details>

* Stylt das Ergebnis, sodass Temperaturunterschiede deutlich erkennbar werden.


  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Das Styling kann unter Properties->Symbology
    unter <i>singleband pseudocolor</i> angepasst werden.

     </ul>
    <br/><br/>

  </details>

Das könnte dann ungefähr so aussehen:
![temperatur_idw_pow2](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_08/temperatur_idw_pow2.PNG)

*(Wer findet den Fehler in dieser Abbildung? Welche Messstation liefert einen möglicherweise falschen Wert?)*
