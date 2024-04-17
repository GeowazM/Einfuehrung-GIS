# Georeferenzierung
* *Raster >> Georeferenzierung* (ggfs. Erweiterung GDAL-Georeferenzierung installieren)

## Wichtiges zur Georeferenzierung
Ziel der Georeferenzierung ist es, einen Geodatensatz ohne Realwelt-Koordinaten anhand von Referenzdaten mit Realweltkoordinaten so zu übersetzten, dass danach ein räumlicher Bezug hergestellt ist. Dabei wird das Koordinatensystem des zu georeferenzierenden Geodatensatzes anhand von Passpunkten modifiziert: mithilfe von Rotation(Drehung), Translation(Verschiebung) und Skalierung(Dehnung/Stauchung) und ggf. Entzerrung wird der Geodatensatz räumlich verortet.

Wichtig für die Übung sind zwei Methoden:
1. Georeferenzieren auf Grundlage einer analogen Karte:
  * Bedingungen:
    * KNE muss bekannt sein
    * Mindestens 4 Koordinatenpunkte müssen bekannt sein
    * Pixelwerte müssen auf Meterangaben skaliert werden
  * als Passpunkte werden die Schnittpunkte vom Gitternetz des zugrundeliegenes KNE verwendet
  * Vorteil: Schnittpunkte genau in Karte ablesbar und damit Passpunkte präzise setzbar
2. Georeferenzieren auf Grundlage eines Luftbilds:
  * Passpunkte wählen anhand von gut verortbaren Orten in den beiden Datensätzen

Zentral für die Georeferenzierung sind Passpunkte, anhand derer von QGIS eine Regression vorgenommen wird. Die Genauigkeit der Georeferenzierung steht und fällt daher mit der Genauigkeit der Passpunkte. Die gewählten Passpunkte sollten daher drei Eigenschaften erfüllen – sie sollten
* ausreichend viele sein (→ Mindestanzahl der Passpunkte erfüllen→RMS-Fehler bestimmbar)
* gut verteilt sein (→ je näher zusammen, desto weniger aussagekräftig der RMS-Fehler für Genauigkeit der Georeferenzierung)
* möglichst gut zu verorten sein (→ exaktere Übereinstimmung der Passpunkte)

Je nachdem, wie gut diese Eigenschaften erfüllt sind, wirkt sich dies auf die Genauigkeit der Übersetzung aus. Diese wird von QGIS durch den RMS-Fehler berechnet – je niedriger dieser ist, desto genauer die Georeferenzierung, sofern die obigen Bedingungen erfüllt sind.

## Vorgehen in QGIS
Reihenfolge in der Regel:
1. [nicht-georeferenziertes Bild öffnen](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#bild-oeffnen-und-zielprojektion-festlegen)
2. [Zielprojektion festlegen](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#bild-oeffnen-und-zielprojektion-festlegen)
3. [Transformationseinstellungen wählen](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#transformationseinstellungen)
4. [Passpunkte setzen](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#passpunkte-setzen-und-speichern)
5. [Passpunkte speichern](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#passpunkte-setzen-und-speichern)
6. [Georeferenziertes Bild speichern](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#georeferenziertes-bild-speichern)
7. Georeferenzierung überprüfen

* [Weitere Ressourcen](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#weitere-ressourcen)
* [Allgemeine Fehlerhinweise](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#allgemeine-fehlerhinweise)

## Bild oeffnen und Zielprojektion festlegen
* Raster einladen und auf Nachfrage die Zielprojektion festlegen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_set_projection.mp4"></video>

**Hinweis:**
Wenn das Programm die Zielprojektion nicht von alleine abfragt, müssen die Einstellungen zu den KBS geändert werden.
Das funktioniert unter *Einstellungen/Settings* in den Toolbars, *Optionen/Options* und dann unter dem Reiter *KBS/CRS*. In diesem muss unter *KBS für neue Layer/CRS for new layers* die Option *KBS abfragen/Prompt for CRS* gewählt werden.

![Einstellungen_KBS-abfragen](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/d5872200508a16e8cd9f0a8f678566fc/Einstellungen_KBS-abfragen.png)![Einstellungen_KBS-abfragen_01](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/bf065093109e2512911bfa9d77e3f77a/Einstellungen_KBS-abfragen_01.png)

## Transformationseinstellungen
* Koordinatentransformation wählen
* Resampling Methode wählen
* Output-Pfad wählen

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_transformation_settings.mp4"></video>

**Praktische Hinweise:**
* wenn das Raster nur gedreht, skaliert und verschoben werden muss *Polynom 1. Grades*
* wenn das Raster gekrümmt oder gebeugt werden muss *Polynom 2. oder 3. Grades*
* Für die Zahl der Passpunkte gilt:
  * Min. Zahl Passpunkte 𝑚=(((𝑡+1)(𝑡+2)))/2   (t = Grad d. Transformation)
  * Das mathematisch „beste“ Modell wird erreicht, wenn exakt die erforderliche Zahl m verwendet wird (RMS-Fehler = 0)
  * Geographisch bessere Ergebnisse werden erzielt, wenn leicht mehr Punkte gesetzt werden, Grund: Punkte werden nicht perfekt gesetzt

## Passpunkte setzen und speichern
* Passpunkte sollten gleichmäßig verteilt sein, da sonst eine lokal fehlerhafte Transformation droht
* Passpunkte sollten so präzise wie möglich platziert werden
* Lieber mäßig viele gute Punkte, als viele schlecht platzierte!

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_set_points_grid.mp4"></video>
* Passpunktkoordinaten im Kartengrid ablesen und eintragen


<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_set_points_from_layer.mp4"></video>
* Passpunktkoordinaten anhand eines anderen Layers wählen


## Georeferenziertes Bild speichern
* Bild speichern
* Datei öffnen und Georeferenzierung überprüfen
* in unserem Beispiel zeigt das Ergebnis eine unterschiedliche Güte für verschiedene Regionen (z.B. relativ gut im zentralen Teil, weniger gut in Nord- und Südamerika)

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_save.mp4"></video>

## Weitere Ressourcen:
* [Digital Geography Tutorial: wie georeferenziere ich eine gescannte Karte in QGIS?](http://de.digital-geography.com/QGIS-tutorial-teil-1-wie-georeferenziere-ich-eine-gescannte-karte-mit-QGIS/)

## Allgemeine Fehlerhinweise
Fehler können unter anderem zu Stande kommen durch:
* fehlerhaftes Ablesen der Koordinaten (beim Ablesen von Passpunktkoordinaten im Kartengrid)
* eine fehlende Übereinstimmung zwischen Projekt-KBS, KBS des georeferenzierten Layers und übrigen Layern vor Beginn des Georeferenzieren
