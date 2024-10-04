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

First install JupyterLab to run the notebook.

```bash
pip install jupyterlab
```
Next start JupyterLab Server

```bash
jupyter lab
```

Jupyter Lab will open in the browser. If not please try to open http://localhost:8888/lab.

### Setup

To keep your secrets separated from the commited source code - we define them in a `.env` file. You can copy the `.env.example` file as a template. 

```bash
cp .env.example .env
```

### Database (option)

In case you would like to work with a database you can spin-up a MySQL Database with Docker.
The `docker-compose` file relays on configured values in the `.env` file.

```bash
docker-compose up db
```
