# :world_map: Urbaner Entwicklungsplan
:white_check_mark: Georeferenziertes Rendering erstellen und als Web-Map publizieren mit Standortermittlung.

## :computer: Link [https://stadtentwicklung.github.io/map2/)

### :camera_flash: Screenshot:
![Screenshot der GitHub-Pages App](https://raw.githubusercontent.com/stadtentwicklung/map2/master/img/screenshotApp.PNG)

## :rocket: Entstehungsprozess

### :compass: Grunddaten herstellen
Geometrien aus dem amtlichen Kataster (ATKIS)--- der Landesvermessung--- bilden die Ausgangsdaten. In Brandenburg stehen diese umfangreichen Vektordaten zum Teil kostenfrei zum Download bereit. QGIS--- ist eine freie Software für die Geodatenverarbeitung und importiert diese Daten ideal zur Analyse und Anpassung. Die Vektordaten sind partiell überarbeitet. Die Flächennutzungstypen und Straßenklassen sind aus den Sachdaten gefiltert. Diese sortierten Kategorien erhalten passende Farbwerte. Als Inspirationsquelle dient ein thematischer Plan von Köln (siehe Bild------). Es ist unbedingt empfehlenswert, eine grafische Zielvorstellung zu nutzen. Des Weiteren sind Geometrien von thematisch wichtigen Projektgebieten mit QGIS--- erstellt und visualisiert. Die Straßenvektoren liegen über allen Flächengeometrien. Häusergeometrien sind ebenfalls aus dem frei zugänglichen Kataster (ALKIS)---. Das erste Bild aus der Workflow-Collage zeigt die Zusammenstellung. Für das finale Ergebnis sind mit QGIS-Layout die (1) Flächen inkl. Straßen getrennt von dem (2) Gebäude-Layer exportiert. Die Häuser erhielten im Gegensatz zum Bild die Farbe weiß. In das QGIS--- -Projekt sind zwei Webservices (Digitales Geländemodell--- und Bildbasiertes Digitales Oberflächenmodell---) integriert und jeweils einzeln im unveränderten Layout exportiert. Diese passgenauen Formate dienen der späteren Schattierung beim Rendern. Aus einem der beiden ist vor dem Rendern mit Adobe Photoshop (Ps) eine violett eingefärbet Normalmap mit unterschiedlichen Hell- und Dunkelwerten generiert. Das andere Modell war bereits einfarbig. Diese Werte bilden die z-Werte für Höhen und Tiefen, die für das Rendern zwingend notwendig sind. Eine echte 3D-Szene ist somit nicht erforderlich um Plastizität und Tiefenräumlichkeit zu erzeugen. Abegesehen davon ist weniger Rechenleistung und Renderzeit nötig.
