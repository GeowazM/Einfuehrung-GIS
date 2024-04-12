## Lokale Rasteroperationen
d.h. Rasterwerte berechnen/nutzen ohne Einbezug der Nachbarschaft

## Raster-Calculator nutzen
* Kombination von logischen (`AND`, `OR`) und mathematischen Operatoren (z.B: `=`, `<`, `>`, `+`, `-`, `*`, `/`)
* Kombination von mehreren Raster-Layern (Bändern) bei der Berechnung möglich
* ACHTUNG: alle Bänder mussen gesondert eingeladen werden
* zum Beispiel um NDVI zu berechnen: (NIR - RED)/(NIR + RED)
* Ausdruck: `("Virtual@8"-"Virtual@4")/("Virtual@8" + "Virtual@4")`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_raster_calculator.mp4"></video>

## Selektion
* einfache Auswahl anhand eines Kriteriums
* so kann man zum Beispiel eine Maske erstellen
* Beispiel: potentielle Wasserflächen anhand des NDVI auswählen (nur negative NDVI-Werte wählen)
* Beispiel-Ausdruck: `"ndvi_raster@1" < 0`

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_raster_select.mp4"></video>

## (Re-)Klassifizierung
* einfachster Weg: SAGA-GIS Reclassify simple tool nutzen
* Methode auswählen und Lookup-Table erstellen
* Beispiel: NDVI klassifizieren

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_reclassify_22.mp4"></video>

* Raster-Calculator nutzen (Kombination von mehreren Selektionen)
* Nutzung von verschachtelten Bedingungen
* Beispiel-Ausdruck:
* `("ndvi_raster@1" <= -0.1) * 0 + ("ndvi_raster@1" > -0.1  AND "ndvi_raster@1" <= 0.1) * 1 + ("ndvi_raster@1" > 0.1  AND "ndvi_raster@1" <= 0.4) * 2 + ("ndvi_raster@1" > 0.4) * 3`

* *Values description: The value range of an NDVI is -1 to 1. Negative values of NDVI (values approaching -1) correspond to water. Values close to zero (-0.1 to 0.1) generally correspond to barren areas of rock, sand, or snow. Low, positive values represent shrub and grassland (approximately 0.2 to 0.4), while high values indicate temperate and tropical rainforests (values approaching 1).* ([Quelle: Sentinel Hub](https://www.sentinel-hub.com/eoproducts/ndvi-normalized-difference-vegetation-index))

## Weitere Ressourcen
* [QGIS Doku: Raster Calculator](https://docs.qgis.org/3.4/en/docs/user_manual/working_with_raster/raster_calculator.html)
