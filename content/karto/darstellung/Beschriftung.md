# Beschriftung

**Hinweis:** Die Videos zeigen, wie sich etwas technisch umsetzen lässt. Sie sollen keinesfalls als Beispiele für gelungene kartographische Umsetzung missverstanden werden. Ggf. führen die Beispiele sogar zu kartographisch schlechten Darstellungen. Generell darf man nicht davon ausgehen, dass sich eine gute kartographische Darstellung in wenigen Minuten erstellen lässt.

## Einfache Beschriftung
* jedes Feature kann mit Werten aus der Attributtabelle beschriftet werden
* Rechtsklick auf Layer --> Labels

### Automatische Platzierung aller Feature
* automatische Platzierung von Labels funktioniert manchmal nur semi-optimal, geht dafür aber sehr einfach und schnell

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads//9b0c573d39828f390da503e3ae43cdc2/single_label.webm"></video>


### Regel-basierte Beschriftung
* Anhand von Attributen werden feature gefiltert und nur diese beschriftet.
* Attribut für Filter und Beschriftung können unterschiedlich sein

Filter mit Text Attribut

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/eefc961d4c7811badce7aac7734d39a1/rule_based_label.webm"></video>

Fitler mit numerischem Attribut

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/e7d538e883d79206486f885d79585a1b/rule_based_label_numeric.webm"></video>


### Manuelle Platzierung
* man startet mit einer automatischen Platzierung und passt dann die Position manuell an
* ermöglicht kartographisch besser platzierte Label, nimmt aber oft sehr viel Zeit in Anspruch
* Nutzung der *Labeling Toolbar*

![labeling_toolbar](https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/img/labeling_toolbar.PNG)


<!-- ![qgis_labels_by_hand_video](uploads/videos/qgis_labels_by_hand.mp4) -->
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/905376dcc0bb10fee52ed4081c7033a5/callouts_label.webm"></video>