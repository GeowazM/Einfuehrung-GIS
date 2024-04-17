# Häufige Fragen und Fehlerquellen

## Layeranzeige
*Mein **Layer** in QGIS wird nicht angezeigt, bzw. Layer, die sich eigentlich an derselben Position befinden sollten liegen nicht aufeinander.*

Probleme mit verschwundenen oder verschobenen Layern liegen meist mit **a) nicht übereinstimmenden KBS in Layern und Projekt**, oder b) **fehlerhaftem Reprojizieren** zusammen. Um dieses Problem zu lösen, kontrolliert also **a)** am besten zuerst in den Eigenschaften der Layer (Rechtsklick, *Eigenschaften*, unter dem Reiter *Information*), in welcher Projektion diese vorliegen, und im Status Bar, unten rechts, welches Projekt KBS/CRS eingestellt ist. Behebt dann etwaige Diskrepanzen durch Umprojizieren der Layer, oder Ändern der Einstellung des Projekt KBS/CRS. Beachtet **b)** beim Reprojizieren genau das Vorgehen, welches im Wiki unter [Projektionen](/content/gis/01_karto-basics/qgis-Projektionen) beschrieben wird. Fehler entstehen häufig, wenn *KBS setzen* und kein Reprojiziertool verwendet wird. Habt ihr den Verdacht, dass euer Umprojizieren fehlerhaft verlaufen ist, löscht alle betroffenen Layer aus GIS, ladet die Daten erneut herein und projiziert dann neu um. Im Zweifel müssen die Daten unter Umständen auch frisch heruntergeladen werden.

## Layerfenster
*Ich habe mein **Layerfenster** aus Versehen geschlossen. Wie kann ich es wieder öffnen?*

Das Layerfenster kann ganz einfach unter *View*, *Panels*, *Layers* wieder geöffnet werden.

![Geschlossenes_Layerfenster](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/5c84e13a2c16fc7a8fdc6b5a7892c68d/Geschlossenes_Layerfenster.png)

## Ungültige Geometrien (Invalid Geometry)
Bei der Fehlermeldung *Ungültige Geometrien* kann es sein, dass Vektordateien im Laufe des Verarbeitungsprozesses oder des Herunterladens "verrutscht" sind (etwa, dass die Linien von Polygonen nicht mehr exakt aufeinander passen). Mit dem Tool ***Fix Geometries*** können diese Fehler in den Geometrien behoben werden.

## Vektorwerkzeuge fehlen
Falls die Vektorwerkzeuge in QGIS nicht mehr angezeigt werden, kann es sein, dass diese in den *Erweiterungen/Plugins* nicht mehr installiert sind.
Diese können folgendermaßen wieder aktiviert werden:

![image](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/70399029d3cb0111dbd3ec0dbcaf49be/image.png)

*Erweiterungen/Plugins*, *Erweiterungen verwalten und installieren/Manage and Install Plugins*, dann unter dem Reiter *Alle/All* oder *Installiert/Installed* die Processing Tools suchen und den Haken wieder setzen.

## Werkzeugkasten
*Wie finde ich den **Werkzeugkasten** / die **Toolbox** bei QGIS?*

Wenn der Wekrzeugkasten nicht in der Toolbar zu finden ist (siehe Abbildung 1), kann er ganz einfach unter *View*, *Panels*, *Layers* wieder angezeigt werden (siehe Abbildung 2).

![Geschlossene_Toolbox_01](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/28e62131a69bcff19d5ebd9017d17f9b/Geschlossene_Toolbox_01.png)  
*Abbildung 1*


![Geschlossene_Toolbox](https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/1e47cd6872f4e40e8f4b3560274ea3d6/Geschlossene_Toolbox.png)  
*Abbildung 2*

## Georeferenzieren
Allgemeine Fehlerhinweise zum [Georeferenzieren](/content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#allgemeine-fehlerhinweise) finden sich unter dem Haupteintrag zu diesem Thema.
