# Übung 9
## Ziel der Übung
* Workflows automatisieren

## Wiki:
* [Automatisierung](/exercise_9/qgis-Automatisierung)


## Daten
Ladet euch [die Daten herunter](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_09/exercise_09.zip) und speichert sie auf eurem PC. Legt einen lokalen Ordner (nicht auf einem Netzlaufwerk wie zum Beispiel "Q://Abgabe") an und speichert dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.)
* Straßen-Layer (Quelle: [OpenStreetMap and Contributors](https://www.openstreetmap.org))
* Hotels-Layer (Quelle: [OpenStreetMap and Contributors](https://www.openstreetmap.org))

## Kontext
Ihr möchtet in Zukunft wiederkehrend den vom Verkehr beeinträchtigten Bereich rund um Hotels berechnen. Dabei möchten ihr auch Parameter variieren. Erstellt hierfür ein geeignetes Werkzeug.

## Aufgabe
## Aufgabe 1: Modell erstellen
Erstellt ein Modell, welches

* einen Punkt- und einen Linienlayer einlesen kann

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Öffne den <b>Modelbuilder</b> und wähle auf der linken Seite <i>Inputs</i> aus. Wähle nun jeweils einmal als Parameter "Vector layer" aus, gib dem Input einen
		sinnvollen Namen (z.B. Roads/Hotels) und wähle als <i>Geometry type</i> entsprechend "Point" oder "Line" aus.

     </ul>
    <br/><br/>

  </details>

* die Punkte mit einem frei wählbaren Pufferabstand puffert (der von Hotels oder anderen Einrichtungen direkt erreichbare Bereich)

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
		Erstelle einen neuen <i>Input</i> diesmal als Parameter "Number". Bennene sie sinnvoll und wähle als <i>Minimum value</i> 0 aus, da ein kleinerer Buffer nicht möglich ist.
		Wähle nun anstatt <i>Inputs</i> <i>Algorithms</i> aus und suche nach der Funktion <b>Buffer</b>. Hier wählst du als <i<Inputlayer</i> den Pointlayer, der als Input übergeben wird,
		und kannst bei dem Feld für den <i>Input</i> links danaben auf das Kästchen drücken und dort <i>Model input</i> auswählen. Anschließend kann im Feld der <i>Model input</i> für die <i>Line buffer distance</i> übergeben werden.

     </ul>
    <br/><br/>

  </details>

* Die Linien mit einem zweiten frei wählbaren Pufferabstand puffert (welcher den vom Lärm beeinflussten Bereich rund um Straßen repräsentiert)

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
		Erstelle einen neuen <i>Input</i> diesmal als Parameter "Number". Bennene sie sinnvoll und wähle als <i>Minimum value</i> 0 aus, da ein kleinerer Buffer nicht möglich ist.
		Wähle nun anstatt <i>Inputs</i> <i>Algorithms</i> aus und suche nach der Funktion <b>Buffer</b>. Hier wählst du als Inputlayer den Linelayer, der als Input übergeben wird,
		und kannst bei dem Feld für den <i>Input</i> links danaben auf das Kästchen drücken und dort <i>Model input</i> auswählen. Anschließend kann im Feld der <i>Model input</i> für die <i>Point buffer distance</i> übergeben werden.

     </ul>
    <br/><br/>

  </details>

* die Schnittmenge dieser Puffer berechnet

  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Diesmal links unter <i>Algorithms</i> die Funktion <b>Clip</b> auswählen. Dort als die beiden Inputlayer jeweils das Ergebnis der beiden Bufferalgorithmen auswählen,
		indem wieder links auf das Kästchen gedrückt wird und <i>Algorithm Output</i> ausgewählt wird.

     </ul>
    <br/><br/>

  </details>

* abschließend noch einen *Dissolve* ausführt


  <details>
  <summary>Lösung</summary>
    <br/>
    <ul>
    <li>
    Wieder links unter <i>Algorithms</i> die Funktion <b>Dissolve</b> auswählen, das Kästchen beim Inputlayer auf <i>Algorithm output</i> umstellen und das Ergebnis
		der Clipfunktion auswählen. Diesmal beim Model Ouput unter <i>Dissolved</i> einen Namen eintragen. Dies ist dann der Output, wenn das gesamte Modell ausgeführt wird.

     </ul>
    <br/><br/>

  </details>

## Aufgabe 2: Modell ausführen
* nutzt euer Modell um die folgende Parameterkombinationen zu testen
  * Hotel-Buffer: 100m, Straßen-Buffer: 50m
  * Hotel-Buffer: 100m, Straßen-Buffer: 100m
  * Hotel-Buffer: 150m, Straßen-Buffer: 200m

So oder ähnlich könnte euer finales Modell aussehen:
![model](https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/raw/master/exercise_09/model.PNG)
