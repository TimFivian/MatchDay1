# MatchDay Scoreboard 🏒

Amateur Floorball Scoreboard — läuft komplett im Browser, kein Server nötig (ausser lokalem Dev-Server).

## Projektstruktur

```
/
├── index.html          # Startseite mit Links zu Display & Controller
├── controller.html     # Spielsteuerung (Tore, Uhr, etc.)
├── controller.js
├── controller.css
├── display.html        # Anzeigetafel (Vollbild, z.B. zweiter Monitor)
├── display.js
├── display.css
├── teams.json          # Teamdaten & Logos
├── *.png               # Team-Logos (direkt im Root-Ordner)
└── README.md
```

## Starten

Da `fetch()` aus Sicherheitsgründen nicht über `file://` funktioniert, brauchst du einen lokalen Webserver:

```bash
# Option 1: Node.js
npx serve .

# Option 2: Python
python3 -m http.server 8000
```

Dann im Browser: `http://localhost:3000` (oder Port 8000 bei Python)

## Nutzung

1. `index.html` öffnen
2. **Display** auf zweitem Monitor/Beamer öffnen
3. **Controller** auf eigenem Gerät öffnen
4. Liga & Teams auswählen → „Spiel starten"
5. Tore & Uhr über den Controller steuern — Display aktualisiert sich automatisch via `localStorage`

## Teams hinzufügen

In `teams.json` neuen Eintrag hinzufügen:

```json
{
  "name": "Mein Team",
  "short": "MTM",
  "league": "NLB",
  "logo": "meinteam.png"
}
```

Logo-PNG direkt in den Root-Ordner legen.
