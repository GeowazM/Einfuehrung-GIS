# Projektionen

## Projektion eines Vektor-Layers ändern
* Vector --> Data Management Tools --> Reproject Layer
* Ziel-Projektion auswählen
* Dateinamen und Speicherort angeben
* in den Eigenschaften des erstellten Layers die Projektion überprüfen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_reproject_vector.mp4"></video>

## Projektion eines Raster-Layers ändern
* Raster --> Projections --> Warp (Reproject)
* Ziel-Projektion auswählen
* Resampling Methode auswählen
* Dateinamen und Speicherort angeben
* in den Eigenschaften des erstellten Layers die Projektion überprüfen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/uploads/QGIS/videos/qgis_reproject_raster.mp4"></video>

## Hinweis
Die Verwendung der hier genannten Tools ist notwendig, um den Layer korrekt zu reprojezieren, das heißt eine Änderung in den Daten und nicht nur in der Darstellung zu bewirken. Wenn die Funktion "KBS setzen" oder ein alleiniges Umstellen der Projektion in der Kartenansicht (Map Canvas) vorgenommen wurde, kann es sein, dass **Layer verschwinden**. In diesem Fall sollte geprüft werden, ob *a)* das in der Kartenansicht eingestellte KBS mit dem der Daten (kann unter *Eigenschaften* abgerufen werden) übereinstimmt, und *b)* ob die Reprojektion korrekt vorgenommen wurde (bei Fehlern in diesem Punkt sollten die entsprechenden Daten aus dem GIS gelöscht, neu hereingeladen, und korrekt reprojeziert werden).

## Weitere Ressourcen
* [QGIS-Doku: Reprojecting and Transforming Data](https://docs.qgis.org/3.4/de/docs/training_manual/vector_analysis/reproject_transform.html)
