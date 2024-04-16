# QGIS-Book

Das Buch ist online verfügbar unter: https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/

Für die Entwicklung:
* Klonen Sie das Repository: `git clone https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book`
* Richten Sie eine Python-Umgebung ein, z.B. `python3 -m venv venv`
* Aktivieren Sie die Umgebung: `source venv/bin/activate`
* Installieren Sie die Abhängigkeiten: `pip install -r requirements.txt`
* `cd gis-training-resource-center` !Erstellen Sie die venv nicht innerhalb des Repositories, da sonst der Build-Befehl versuchen wird, Quelldateien aus /venv zu kompilieren.
* Führen Sie Ihre Änderungen am Buch im `contents`-Verzeichnis durch.
* Bauen Sie es lokal mit `jupyter-book build .`.
