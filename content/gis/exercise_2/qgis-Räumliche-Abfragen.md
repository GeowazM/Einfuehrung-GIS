# Räumliche Abfragen

## Manuelle Auswahl
* ein Feature nach dem anderen durch anklicken selektieren

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_features_by_click.mp4"></video>

* Features per Polygon selektieren

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_features_by_polygon.mp4"></video>

## Select by Location
Es gibt verschiedene räumliche Abfrage-Operationen:
* Intersect
* contain
* disjoint
* equal
* touch
* overlap
* are within
* cross

* z.B. alle Städte in China selektieren (`intersect`)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_location_intersect.mp4"></video>

* z.B. alle Nachbarstaaten Chinas selektieren (`touch`)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_location_touch.mp4"></video>


## Verschiedene räumliche Abfragen kombinieren
* *adding to current selection* (`OR`)
* *selecting within current selection* (`AND`)
* *remove from current selection* (`AND NOT`)

* z.B. alle Staaten, welche an China *und* Indien grenzen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_location_combined.mp4"></video>
