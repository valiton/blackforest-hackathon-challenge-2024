# Black Forest Hackathon 2024 - Challenge

### Unterstützung für den InStyle Community Manager 

Als Community Manager bei InStyle ist es deine Aufgabe, täglich Inhalte auf verschiedenen Social-Media-Plattformen wie 
Facebook, Instagram und TikTok zu erstellen, zu veröffentlichen und zu moderieren. Derzeit wird ein großer Teil der Arbeitszeit 
darauf verwendet, Kommentare zu erfassen, zu analysieren, darauf zu reagieren oder unangemessene Inhalte zu löschen. 
Ziel ist es, diesen Prozess in Zukunft effizienter und automatisierter zu gestalten, sodass sich der Community Manager 
stärker auf die Markenkommunikation konzentrieren kann. 

## Schwerpunkte 

* **Aussortieren unerwünschter Kommentare**, z.B.:
  * Hate Speech (kann auch sarkastische Inhalte umfassen) 
  * Werbung (Eigenwerbung für Produkte)
  * Ideologische Inhalte
  * Bots (Erkennung von Trollen)
* **Identifikation von Kommentaren**, die eine Antwort des Community Managers erfordern 
* **Analyse des Feedbacks**: Wie wurde der Inhalt vom Publikum aufgenommen? Positiv/negativ? Was kann zukünftig verbessert werden? (Sentiment-Analyse) 
* **Normalisierung von Kommentaren**, die in verschiedenen Sprachen, Schriftarten und mit Emojis verfasst sind
* **Effiziente Bearbeitung von Kommentaren**, insbesondere bei einer hohen Anzahl (Zusammenfassungen statt einzelner Betrachtungen) 
* **Inkrementelle Analyse neuer Kommentare** über einen bestimmten Zeitraum (optional) 
## Daten 

Für die Challenge stellen wir euch Exporte von Kommentaren unserer Community zu verschiedenen TikTok Video Posts im CSV-Dateiformat bereit.

## Bonus 

Habt Ihr noch weitere Ideen wie man den Community Manager weiter unterstützen kann? Wir sind gespannt davon zu hören.

## Get Started

Jeder Anfang ist schwer. Wir haben euch ein Jupyter Notebook als Einstiegspunkt bereitgestellt.
Ihr könnt dieses ganz nach Belieben anpassen oder ganz eigene Wege gehen.

### Installation

Damit das Notebook in einer eigenen Umgebung läuft ist es Sinnvoll das Ganze in einem Virtuellen Environment auszuführen.
Das Virtuelle Environment kann innerhalb des Projektverzeichnisses wie folgt erstellt werden:

```bash
python -m venv ./.venv
```

Anschließend muss die Virtuelle Umgebung mit folgendem Kommando aktiviert werden:

```bash
source .venv/bin/activate
```

Jetzt kann man JupyterLab in der Virtuellen Umgebung installieren. JupyterLab wird benötigt zum ausführen der Notebooks.

```bash
pip install jupyterlab
```
Als nächstes kann der JupyterLab Server mit folgendem Kommando gestartet werden

```bash
jupyter lab
```

Jupyter Lab sollte den Browser automatisch öffnen. Falls nicht dann ruft folgende URL auf: http://localhost:8888/lab

### Setup

Damit Secrets nicht in der Versionsverwaltung gespeichert werden, definieren wir diese in einer separaten `.env` Datei. Hierfür kann die `.env.example` als Vorlage verwendet werden.

```bash
cp .env.example .env
```

### Database (option)

Falls ihr eine Datenbank benutzen möchtet, könnt ihr eine MySQL Datenbank schnell mit Docker hoch fahren. Die `docker-compose` Datei benutzt die Umgebungsvariablen, die in der zuvor erstellten `.env` datei angelegt wurden.

```bash
docker-compose up db
```

### Datenbasis

Die Jupyter Notebooks laden Standardmäßig eine CSV Datei mit dem Namen **comments.csv**. Ihr könnt als Beispiel eine der zur Verfügung gestellten Exportdatei aus dem Zip-Archiv umbenennen und in das Projektverzeichnis mit dem angegebenen Namen ablegen. Dann sollte diese Datei für die Notebooks genutzt werden.
