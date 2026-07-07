# Step 1: GitHub Link kopieren 

# Step 2: Github repository clonen

# Step 3: Vorbereitung

- .env.example zu .env umbenennen und alle Passwörter/Tokens anpassen.
- Für Mosquitto wird eine Konfigurationsdatei unter ./mosquitto/config/mosquitto.conf erwartet (sonst startet er ggf. nicht richtig, da kein Listener konfiguriert ist).
- Für evcc wird eine ./evcc/evcc.yaml benötigt – die Konfiguration ist sehr individuell (Wechselrichter, Ladepunkt, Tarife usw.) und muss selbst erstellt werden.
- Für Flightradar24 wird i.d.R. echte SDR-Hardware (z.B. RTL-SDR Stick) per USB-Passthrough benötigt, sowie ein Sharing-Key von Flightradar24.
- Für Traccar wird eine Datei für die Datenbank und ein Ordner für die Logs benötigt
./traccar/
  traccar.xml   ← heruntergeladene Datei hier ablegen
  logs/         ← Verzeichnis manuell anlegen (mkdir traccar/logs)

# Step 4: Container bauen können
docker-compose up -d

# Step 5: Portübersicht

    Portainer https://iot.fritz.box:9443, 8000
    Mosquitto 1883, 9001
    InfluxDB 8086
    Postgres 5432
    MariaDB 3306
    phpMyAdmin http://iot.fritz.box:8081
    Node-RED http://iot.fritz.box:1880
    Grafana http://iot.fritz.box:3000
    Flightradar http://iot.fritz.box:8754
    tar1090 http://iot.fritz.box:8080
    evcc http://iot.fritz.box:7070
    pihole https://iot.fritz.box/admin/login
    Traccar http://iot.fritz.box:8082


