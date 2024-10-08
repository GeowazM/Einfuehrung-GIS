**Hinweis:** Die Videos zeigen, wie sich etwas technisch umsetzen lässt. Sie sollen keinesfalls als Beispiele für gelungene kartographische Umsetzung missverstanden werden. Ggf. führen die Beispiele sogar zu kartographisch schlechten Darstellungen. Generell darf man nicht davon ausgehen, dass sich eine gute kartographische Darstellung in wenigen Minuten erstellen lässt.

Wichtig ist, dass bei der eigenen Arbeit - neben weiteren kartographischen Grundsätzen - die Grundlagen der Farbwahl (Assoziationen, Konventionen, Unterscheidbarkeit der Farben,...), der Paltettenauswahl (sequentiell, divergierend, ungeordnet), der Klassenanzahl (einfarbiger Verlauf maximal 6-8 Klassen, mehrfarbiger Verlauf maximal 10-12 Klassen) und der Klasseneinteilung berücksichtigt werden. Die Standard-"Vorschläge" von QGIS sind i.d.R. ungeeignet.

# Graphische Variablen

n der Kartographie sind graphische Variablen Eigenschaften oder Merkmale, die auf einer Karte dargestellt werden, um Informationen zu vermitteln. Diese Variablen sind entscheidend, um Karten leicht verständlich und informativ zu gestalten. Graphische Variablen können z.B. die Größe, Farbe, Transparenz, Form oder Helligkeit sein. Die effektive Nutzung dieser graphischen Variablen ermöglicht es, komplexe Informationen auf verständliche Weise darzustellen und die Botschaft einer Karte klar zu vermitteln.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/categoriesPointColor.mp4"></video>
Das Video demonstriert den Einsatz anhand von Punktdaten (Flughäfen, die in eine Reihe von Klassen eingeteilt sind). Anschließend werden die Symbole für einzelne Klassen zusätzlich manuell verändert (sowohl hinsichtlich der Größe, als auch hinsichtlich der Farbe).

## Kategorische Daten - nominal oder ordinal skaliert

Bei kategorischen Daten werden die Daten anhand eines Merkmals (hier Farbe) gruppiert und je Gruppe ein Symbol zugewiesen. Dabei wird ein Attributfeld ausgewählt, anhand dessen eindeutiger Werte Gruppen eingeteilt werden. Für fortlaufende Daten (z.B. Lufttemperatur oder Bevölkerungsdichte) eher nicht geeignet, da dann wirklich jeder unterschiediche Wert ein anderes Symbol zugewisen bekommt.

Ein Beispiel für die kategorische Darstellung anhand von Größe und Symbol könnt ihr im obenstehenden sehen; anhand vom Farbe im nachfolgenden Video.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/qgis_symbology_categorized_polygon.mp4"></video>

## Kontinuerliche Daten - intervall oder verhältnisskaliert

Kontinuerliche Werte müssen zunächst in Klassen eingeteilt werden, wofür es unterschiedliche Verfahren gibt. Je nach Verteilung der Daten und je nach gewünschter Aussage sind die einzelnen Verfahren zur Klasseneinteilung besser oder schlechter geeignet.
Neben der Klasseneinteilung steht die Frage nach der Anzahl von Klassen und die Symbolzuordnung im Raum.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/qgis_symbology_graduated_point.mp4"></video>
Eine besondere Art der Darstellung von kontinuierlichen Daten, ist die Choroplethenkarte. Nachfolgende Videos verdeutlichen die einzelnen Arbeitsschritte zur Erstellung dieser.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/chroplethenkarte_kontWerteEinteilen_gdp.mp4"></video>
**Hinweis:** bei Choroplthenkarten dürfen - in den allermeisten Fällen - keine Absolutwerte dargestellt werden! Deswegen wird hier durch die Bevölkerung geteilt und das Bruttosozialprodukt je Einwohner für die Einteilung und Darstellung verwendet. Die Kartendarstellung ändert sich dadurch stark.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/choroplethenkarte_normierung.mp4"></video>
Unterschiedliche Klasseneinteilungen betonen andere Aspekte der Verteilung.

<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/choroplethenkarte_klassifizierung.mp4"></video>
<video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/choroplethenkarte_klassenanzahl.mp4"></video>