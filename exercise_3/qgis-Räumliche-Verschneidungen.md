# Räumliche Verschneidungen

## Clip
* Input Layer: Layer, das zugeschnitten werden soll (z.B. Straßennetzwerk)
* Overlay Layer: z.B. Polygon-Layer der Region (z.B. Grenzen von Heidelberg)
* Beispiel: Schienennetzwerk in Deutschland extrahieren

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_clip.mp4"></video>

## Erase (Difference)
* Input Layer: Layer, aus dem Daten entfernt werden sollen (z.B. Straßennetzwerk)
* Overlay Layer: z.B. Polygon-Layer der Region (z.B. Grenzen von Heidelberg)
* Beispiel: Schienennetzwerk in Deutschland entfernen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_difference.mp4"></video>

## Intersection
* Reihenfolge von *Input Layer* und *Overlay Layer* spielt hier keine Rolle
* Möglichkeit nur bestimmte Felder der Ausgangslayer zu behalten
* Achtung: Attributwerte, welche sich auf Ausgangsflächen beziehen (z.B. Bevölkerungszahl), sind nach dem Intersect nicht mehr aussagekräftig
* Beispiel: Grenzen und Zeitzonen miteinander verschneiden

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_intersect.mp4"></video>

## Symmetrische Differenz
* Reihenfolge von *Input Layer* und *Overlay Layer* spielt hier keine Rolle

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_symmetrical_difference.mp4"></video>

## Union
* Reihenfolge von *Input Layer* und *Overlay Layer* spielt hier keine Rolle

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_union.mp4"></video>
