# Übung 5

## Ziel der Übung
- Daten von OSM herunterladen.
- Atrribute von OSM-Daten anlysieren und nutzbar machen.
- Eine Karte mit OSM-Daten erstellen.

## Wiki:
- [OSM Grundlagen](/exercise_5//home-OSM-Grundlagen)
- [OSM Daten herunterladen](/exercise_5//home-OSM-Daten-herunterladen)

## Aufgaben

1. Ladet euch einen Datensatz mit Bushaltestellen in Heidelberg herunter. Ihr könnt dafür sowohl overpass turbo, als auch das QuickOSM Plug-in von QGIS benutzen.

*Wenn ihr nicht wisst, welche Tags ihr dafür Abfragen könnt, schaut doch mal in das deutsche OSM Wiki
zu [öffentlichem Verkehr](https://wiki.openstreetmap.org/wiki/DE:Map_Features#%C3%96ffentlicher_Verkehr_(Infrastruktur))
und [Transport und Verkehr](https://wiki.openstreetmap.org/wiki/DE:Map_Features#Transport,_Verkehr).*

  <details>
  <summary>Lösung</summary>
  Query Wizard:

    public_transport=platform OR public_transport=station OR amenity=bus_stop

  Overpass QL:

    [out:json][timeout:25];
    (
    node["public_transport"="platform"]({{bbox}});
    way["public_transport"="platform"]({{bbox}});
    relation["public_transport"="platform"]({{bbox}});
    node["public_transport"="station"]({{bbox}});
    way["public_transport"="station"]({{bbox}});
    relation["public_transport"="station"]({{bbox}});
    node["amenity"="bus_stop"]({{bbox}});
    way["amenity"="bus_stop"]({{bbox}});
    relation["amenity"="bus_stop"]({{bbox}});
    );
    out body;
    >;
    out skel qt;

  </details>

2. Ladet den heruntergeladenen Datensatz in QGIS. Schaut euch die Attribut-Tabellen der Layer an und versucht euch einen Überblick zu verschaffen, was für Informationen euch dort zur Verfügung stehen.

3. Eventuell müsst ihr Datensätze von OSM für euren Zweck verkleinern oder vervollständigen.

  <details>
  <summary>Lösung</summary>
  Eine Bushaltestellen Datensatz ist in den meisten Fällen am besten ein Punkt-Layer. Die Linien- und Polygon-Layer könnt ihr also vermutlich löschen.

  Wenn ihr z.B. public_transport=platform abgefragt habt, enthält dieser Datensatz wahrscheinlich auch Bahn-plattformen o.ä.,
  diese könnt ihr etwa über eine Abfrage nach dem "railway" Tag in QGIS aus dem Datensatz löschen, über selektives Layer Styling nur nicht darstellen oder gleich in der Overpass Abfrage ausschließen.

  </details>

4. Erstellt eine Karte, in der nur die Haltestellen von Bussen in Heidelberg zu sehen sind, oder die Bushaltestellen zumindest von anderen ÖPNV Haltestellen klar unterscheidbar sind.
