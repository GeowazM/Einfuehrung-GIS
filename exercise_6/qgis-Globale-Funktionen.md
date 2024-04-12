# Globale Rasteroperationen und Sonstige Funktionen

## Projektion ändern (Warp)
* Ziel Projektion angeben
* die korrekte Resampling-Methode muss dem Datentyp angepasst gewählt werden (z.B. Nearest Neighbor für Kategorien)
* (evtl. einen Wert für NoData Zellen angeben)
* diese Operation erstellt ein neues Raster für welches Form und Größe der Rasterzellen verändert sind

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_warp.mp4"></video>

## Build Virtual Raster
* verschiedene Bänder in einem Raster zusammenführen
* die Bänder haben bereits die gleiche räumliche Ausdehnung
* Beispiel: Bänder der Landsat- oder Sentinel-Daten zusammenführen  

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_build_virtual_raster.mp4"></video>

**Hinweis:**  
Das virtuelle Raster nummeriert seine Bänder beginnend mit der Zahl 1, unabhängig davon welche Bändernummern die eingeladenen Bänder tatsächlich besitzen. Im Video wird ein vollständiger Datensatz verwendet (alle Bänder sind vorhanden). Von diesem werden die ersten acht Bänder im virtuellen Raster zusammengefügt. Folglich ist die Zuordnung 1:1 (Band 1 im Datensatz = Band 1 im virtuellen Raster, usw.). Wird nur ein Teil-Datensatz in ein virtuelles Raster zusammengeführt, zum Beispiel Bänder 4-6, dann ist die Zuordnung verändert (Band 4 im Datensatz = Band 1 im virtuellen Raster, usw.). Es empfiehlt sich daher bei der Erstellung eines virtuellen Rasters aus unvollständigen Datensätzen eine Notiz anzulegen, welche Bänder des Datensatzes welchen Bändern im virtuellen Raster entsprechen.

## Raster zusammenfügen (Mosaik erstellen)
* Raster --> Sonstiges --> Merge
* verschiedene Raster gleichen Typs räumlich zusammenfügen
* die Raster haben eine unterschiedliche räumliche Ausdehnung, sind aber in der Regel benachbart
* Beispiel: ein Höhenmodell aus verschiedenen kleineren ASTER-DEM Rasterdateien erstellen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_merge.mp4"></video>

## Raster Statistiken berechnen
* z.b. Maximalwert, Minimalwert berechnen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_layer_stats.mp4"></video>
