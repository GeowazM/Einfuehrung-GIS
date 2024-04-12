# Darstellung von Rasterdaten

## Single-Band Raster
### Kontinuierliche Darstellung
* z.B. NDVI, Höhenmodell oder Niederschlag

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_display_singleband.mp4"></video>

### Klassifizierte Darstellung, aber kontinuierliche Daten
* z.B. NDVI, Höhenmodell

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_display_singleband_discrete.mp4"></video>

### Klassifizierte Darstellung und kategorisierte Daten
* z.B. NDVI-Kategorien, Landnutzungsraster

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_display_singleband_palleted.mp4"></video>

## Multiband Raster
In Multiband-Rasterdaten zeigen verschiedene Bänder verschiedene Wellenlängenbereiche. Diese Zuordnung variiert für jeden Satelliten und muss daher jeweils selbstständig recherchiert werden. Welche Bänder welchen Wellenlängen für Landsatdaten entsprechen, findet sich beispielsweise unter folgendem [Link](https://de.wikipedia.org/wiki/Landsat_8). Auch für die korrekte Bänderzuordnung für Falschfarbendarstellungen finden sich online Informationen (z.B. [hier](http://blog.imagico.de/uber-falsche-farben/) oder [hier](https://www.esri.com/arcgis-blog/products/product/imagery/band-combinations-for-landsat-8/)).

**Hinweis:**  
In den folgenden Videos werden vollständige Sentinel-Datensätze verwendet. Solltet ihr unvollständige Datensätze (beachtet dazu [diesen](qgis-Globale-Funktionen#build-virtual-raster) Hinweis) und/oder Landsat-Datensätze verwenden, können die Bändernummern aus den Videos nicht einfach übernommen werden!
 
### Echtfarben-Darstellung (RGB)
* in der Regel Darstellung von Satellitendaten (z.B. Landsat oder Sentinel)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_display_multiband_rgb.mp4"></video>

### Falschfarbendarstellung
* z.B. Vegetation oder vergletscherte Gebiete auf Satellitenbildern hervorheben

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_raster_display_multiband_false_color.mp4"></video>

## Weitere Ressourcen
* [Sentinel Hub False Color Darstellung](https://www.sentinel-hub.com/eoproducts/false-color)
