# Geometrieoperationen

## Koordinaten extrahieren
* Extract Vertices
* extrahiert alle Stützpunkte für Linien bzw. Polygone und speichert diese als Punkt-Features

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_geometry_extract_vertices.mp4"></video>

## Länge, Fläche, Umfang berechnen
* Add geometry Attributes Tool
* Berechnet geometrische Attribute der Features
* für Polygon: Fläche, Umfang
* für Linie: Länge
* für Punkt: X-, Y-Koordinaten
* Achtung: bei der Berechnung muss ein **passendes (in der Regel metrisches) Koordinatensystem** angegeben werden; die Einheit, in der die Daten ausgespuckt werden, sind bei einem korrekt gewählten Koordinatensystem gewöhnlicherweise Meter oder Quadratmeter (bei Länge, Umfang, oder Fläche), es empfiehlt sich aber auch die Daten gegebenenfalls zu hinterfragen und evtl. vergleichbare Referenzwerte hinzuzuziehen. 

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_geometry_add_geom_attributes.mp4"></video>

## Mittelpunkt (Centroid) berechnen
* Centroids Tool
* berechnet den Mittelpunkt für Polygon-Features oder Line-Features

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_geometry_centroids.mp4"></video>

## Geometrie vereinfachen (generalisieren)
* Simplify Tool
* z.B. Anwendung des Douglas Peucker Algorithmus zur Vereinfachung von Linienzügen
* Achtung: Dadurch kann die Topologie einzelner Features geändert werden. Es entstehen beispielsweise Lücken zwischen Polygonen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_geometry_simplify.mp4"></video>


## Validität überprüfen
* Check Validity Tool
* ermöglicht fehlerhafte Geometrien zu identifizieren
* Grund für Fehler können beispielsweise *self intersections* sein

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_geometry_check_validity.mp4"></video>

## Bounding Box (Konvexe Hülle berechnen)
* bounding boxes Tool
* (es gibt auch oriented minimum bounding boxes)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_bounding_boxes.mp4"></video>

* convex hull Tool

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_convex_hull.mp4"></video>

## Geometrien aggregieren (Dissolve)
* dissolve Tool
* fasst Geometrien mit gleichen Attributwerten zusammen
* Achtung: in QGIS werden hier die anderen Attribute nicht aggregiert, im Beispiel wird daher der Name nicht korrekt angegeben

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_dissolve.mp4"></video>


## Buffer
* einen Puffer mit einer definierten Distanz berechnen
* Dissolve: überlappen sich 2 oder mehrere Bufferflächen, können diese zusammengefasst werden
* Achtung: Die Einheit der Distanz ist abhängig von der Projektion des Layers, für Buffer braucht man in der Regel ein metrisches Koordinatensystem
* In QGIS gibt es auch die Möglichkeit mithilfe der `Multiple Ring Buffer` Funktion mehrere Bufferinge, mit jeweils der gleichen Distanz zu erstellen. Beim Erstellen eines solchen Layers wird den verschiedenen Ringen in der Attributtabelle jeweils eine ringID zugeordnet, welche hilfreich für weitere Arbeitsschritte ist. 
* Beispiel: Welche Flächen liegen im Umkreis von 100 Kilometer um Großstädte

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_buffer.mp4"></video>

**Hinweis:**  
Bei riesigen "Megabuffern" oder wenn der Abstand der Buffer nur in Grad, und nicht in Metern gewählt werden kann, liegt entweder kein metrisches Koordinatensystem vor, oder es wurde falsch umprojeziert (die Einheit der Buffer hängt vom KBS des Layers ab).