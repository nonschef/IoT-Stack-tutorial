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
