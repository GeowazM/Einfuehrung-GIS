# Weitere Rasterfunktionen

## Rasterdaten zuschneiden
### Clip by Extent
* es wird die Bounding Box des angegebenen Layers genutzt

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_raster_clip_by_extent.mp4"></video>

### Clip by Mask
* es wird die exakte Geometrie des angegebenen Layers genutzt

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_raster_clip_by_mask.mp4"></video>

## Extraktion von Rasterwerten
* Rasterwerte als Attribut von Punkt-Features hinzufügen
* Beispiel: Die Höhe ü.N. für Städte aus einem Rasterlayer extrahieren

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_raster_sample_points.mp4"></video>


## Höhenprofil erstellen
* QGIS Plugin "Profile Tool" installieren
* Rasterlayer im Tool hinzufügen
* Vektorlayer anklicken und hinzufügen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_profile.mp4"></video>

**Hinweis:**
Das Tool *Profile Tool* funktioniert nur, wenn der Linienlayer eine zusammenhängende Linie enthält. Mehrere unverbundene Stücke, wie zum Beispiel nach einem Clip entstehen können, sind im Tool nicht verwertbar.