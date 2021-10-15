# :world_map: Urbaner Entwicklungsplan
:white_check_mark: Georeferenziertes Rendering erstellen und als Web-Map publizieren mit Standortermittlung.

## :computer: Link [https://stadtentwicklung.github.io/map2/)

### :camera_flash: Screenshot:
![Screenshot der GitHub-Pages App](https://raw.githubusercontent.com/stadtentwicklung/map2/master/img/screenshotApp.PNG)

## :rocket: Entstehungsprozess

### :computer: Grunddaten herstellen
Geometrien aus dem amtlichen Kataster (ATKIS)--- der Landesvermessung--- bilden die Ausgangsdaten. In Brandenburg stehen diese umfangreichen Vektordaten zum Teil kostenfrei zum Download bereit. QGIS--- ist eine freie Software für die Geodatenverarbeitung und importiert diese Daten ideal zur Analyse und Anpassung. Die Vektordaten sind partiell überarbeitet. Die Flächennutzungstypen und Straßenklassen sind aus den Sachdaten gefiltert. Diese sortierten Kategorien erhalten passende Farbwerte. Als Inspirationsquelle dient ein thematischer Plan von Köln (siehe Bild------). Es ist unbedingt empfehlenswert, eine grafische Zielvorstellung zu nutzen.

![Plan aus Köln zur Inspiration](https://raw.githubusercontent.com/stadtentwicklung/map2/master/img/inspiration.PNG)

Des Weiteren sind Geometrien von thematisch wichtigen Projektgebieten mit QGIS--- erstellt und visualisiert. Die Straßenvektoren liegen über allen Flächengeometrien. Häusergeometrien sind ebenfalls aus dem frei zugänglichen Kataster (ALKIS)---. Das erste Bild aus der Workflow-Collage (siehe unten) zeigt die Zusammenstellung. Für das finale Ergebnis sind mit QGIS-Layout die (1) Flächen inkl. Straßen getrennt von dem (2) Gebäude-Layer exportiert. Die Häuser erhielten im Gegensatz zum Bild die Farbe weiß. In das QGIS--- -Projekt sind zwei Webservices (Digitales Geländemodell--- und Bildbasiertes Digitales Oberflächenmodell---) integriert und jeweils einzeln im unveränderten Layout exportiert. Diese passgenauen Formate dienen der späteren Schattierung beim Rendern. Aus einem der beiden ist vor dem Rendern mit Adobe Photoshop (Ps) eine violett eingefärbet Normalmap mit unterschiedlichen Hell- und Dunkelwerten generiert. Das andere Modell war bereits einfarbig. Diese Werte bilden die z-Werte für Höhen und Tiefen, die für das Rendern zwingend notwendig sind. Eine echte 3D-Szene ist somit nicht erforderlich um Plastizität und Tiefenräumlichkeit zu erzeugen. Abegesehen davon ist weniger Rechenleistung und Renderzeit nötig.

![Screenshot Workflow](https://raw.githubusercontent.com/stadtentwicklung/map2/master/img/workflow.PNG)

:cinema: Schattierungen rendern
Die Datei (1) Flächen inkl. Straßen mit Gleisen und die Datei (2) Gebäude liegen in Ps in getrennten Ebenen übereinander. Dadurch kann nur den Gebäuden bereits vor dem Rendern Schatten zugewiesen werden. Die Ebenen sind anschließend zusammengeführt und über die 3D-Funktion auf Grundlage der beiden Höhenbilder mit Schattierung gerendert. Die Workflow-Collage zeigt das Bild jeweils vor und nach den Renderprozessen, die insgesamt weniger als zwei Stunden dauerten.

:art: Grafiken layouten
Mit Adobe Illustrator sind die grafischen Elemente sowie Texte erzeugt, die das fertige Layout ergeben. Überzeigende Grafikelemente zu erstellen ist aufwendig aber notwendig, um die verschiedenen Symboliken in Bezug auf deren inhaltlichen Aussagen abzustimmen.

:octocat: Karte publizieren
Das Ergebnis ist mit QGIS--- wieder georeferenziert für eine Bereitstellung als Webmap. Dafür bietet QGIS--- die Funktion GDAL2TILES--- an. Als Präsentationsplattform eigent sich u.a. Leaflet---, wobei das Bild dann zwingend im Koordinatensystem mit EPSG:3857 (WGS84) georeferenziert werden muss. Siehe hierzu die Problematik auf Stackoverflow--- (vgl. Abbildung).

![Gdla2Tiles with EPSG:25833 und EPSG:3857](https://raw.githubusercontent.com/stadtentwicklung/map2/master/img/stackoverflow.PNG)

Nach dem Speichern der Tiles als Webmap-Paket, wurde der HTML-, CSS- und JavaScript-Code individuell verfeinert z.B. mit der Funktion Standortermittlung. Alle Veränderungen lassen sich lokal über den Browser beurteilen. Das überarbeitete Paket ist in dieses Repository auf GitHub über die Kommandozeile hineingeladen (das Projekt besteht auf Grund der Tiles aus fast 500 Dateien, welche nicht mit Drag & Drop platziert werden können). Die aktivierte Funktion GitHub-Pages--- erlaubt jetzt, die Karte online über eine Domain--- aufzurufen.
