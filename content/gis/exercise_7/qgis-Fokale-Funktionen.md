# Fokale Rasteroperationen
d.h. Rasterwerte berechnen/nutzen mit Einbezug der Nachbarschaft

## Generalisierung, Tiefpassfilter (Glätten)
* berechnet den Durchschnittswert der Nachbarpixel
* Extrema werden dadurch geglättet
* es muss eine Nachbarschaft angegeben werden (im Beispiel: 15)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_raster_generalize.mp4"></video>

## Reliefanalysefunktionen
* Achtung: die Projektion des Raster ist hier sehr wichtig um aussagekräftige Ergebnisse zu erzielen. Hier sollte immer eine metrische Funktion angewandt werden.
* für metrische Projektionen beträgt der Z-Faktor "1", wenn man eine andere Projektion nutzt muss der Z-Faktor angepasst werden

### Hangneigung (Slope)
* wird in ° angegeben
* Minimum: 0° (flach), Maximum: 90° (senkrechte Wand)
* für eine Angabe in % muss die Umrechnung in einem seperaten Schritt erfolgen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_slope.mp4"></video>

### Exposition (Aspect)
* wird angegben als Abweichung von Norden in ° (0°-360°)
* z.B. Südseite: 180°

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_aspect.mp4"></video>

### Krümmung (Curvature)
* SAGA-GIS Tool "Slope, Aspect, Curvature"
* auswählen welche Dateien erstellt werden sollen (*Skip Output* für die anderen angeben)
* Profilkrümmung (englisch: profile)
* Horizontalkrümmung (englisch: planform/plan)
* am Beispiel erkennt man z.B. dass Seen keine Krümmung aufweisen, die Uferkanten jedoch deutlich

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_curvature.mp4"></video>

Hintergrundinfo:
* Eine positive Profilkrümmung gibt eine konkave Krümmung an, was die Fließgeschwindigkeit von abfließendem Wasser erhöht.
* Bei der horizontalen Krümmung sind hingegen negative Werte von größerer Bedeutung für die Erosion, da dies Wasserflüsse bündelt und so die Fließgeschwindigkeit und den Bodenabtrag noch stärker beschleunigt

### Schummerung (Hillshade)
* hier könnt ihr mit dem Z-Faktor spielen und einen angepassten visuellen Eindruck zu erzielen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_hillshade.mp4"></video>
