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

Um das Notebook auszuführen muss zuertst JupyterLab installiert werden.

```bash
pip install jupyterlab
```
Als nächstes kann der JupyterLab Server mit folgendem Kommando gestartet werden

```bash
jupyter lab
```

Jupyter Lab sollte im browser sich automatisch öffnen. Falls nicht dann ruft folgende URL auf: http://localhost:8888/lab.

### Setup

Damit secrets nicht in der Versionsverwaltung gespeichert werden, definieren wir diese in einer separaten `.env` Datei. Hierfür kann die `.env.example` als Vorlage verwendet werden.

```bash
cp .env.example .env
```

### Database (option)

Falls ihr eine Datenbank benutzen möchtet, könnt ihr eine MySQL Datenbank schnell mit Docker hoch fahren. Die `docker-compose` Datei benutzt die Umgebungsvariablen, die in der zuvor erstellten `.env` datei angelegt wurden.

```bash
docker-compose up db
```
