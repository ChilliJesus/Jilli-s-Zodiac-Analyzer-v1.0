# KOSMOS — Astrologische Natal-Analyse PWA

## Was ist das?
Eine vollständige astrologische Horoskop-App als Progressive Web App (PWA).
Sie berechnet echte Planetenpositionen und erstellt eine ~20-seitige KI-Deutung.

## Features
- ☉ Echte Planetenberechnung (Sonne, Mond, Merkur, Venus, Mars, Jupiter, Saturn, Uranus, Neptun, Pluto)
- ⌂ Häusersystem nach Placidus
- △ Aspektenberechnung (Konjunktion, Opposition, Trigon, Quadrat, Sextil, Quincunx)
- ⊙ Interaktives Horoskop-Rad (Canvas)
- ✦ KI-gestützte ~5000-Wörter Deutung via Claude API (Streaming)
- 📱 Als App auf Android/iOS installierbar
- 🌙 Offline-fähig (nach erstem Laden)

## Auf Android als App installieren

### Methode 1 — Chrome (empfohlen)
1. Kopiere alle 3 Dateien auf einen Webserver oder nutze einen lokalen Server
2. Öffne die Seite in Chrome auf deinem Android-Gerät
3. Tippe auf die drei Punkte (⋮) oben rechts
4. Wähle **"Zum Startbildschirm hinzufügen"**
5. Die App erscheint wie eine native App auf deinem Homescreen!

### Methode 2 — Lokaler Server (kein Hosting nötig)
Auf deinem PC:
```
npx serve .
```
Dann im lokalen Netzwerk auf dem Handy öffnen: `http://192.168.x.x:3000`

### Methode 3 — GitHub Pages (kostenlos, dauerhaft)
1. GitHub-Account erstellen
2. Neues Repository anlegen
3. Alle 3 Dateien hochladen
4. Settings → Pages → "Deploy from branch: main"
5. Deine App ist unter `https://deinname.github.io/kosmos` erreichbar

## Claude API-Schlüssel
1. Gehe zu https://console.anthropic.com
2. Account erstellen / einloggen
3. API Keys → "Create Key"
4. Den Key in der App eingeben (wird NICHT gespeichert, nur lokal verwendet)

## Dateien
- `index.html` — Die komplette App
- `manifest.json` — PWA-Konfiguration
- `sw.js` — Service Worker (Offline-Support)

## Technische Details
- Planetenberechnung: Astronomische Algorithmen (Jean Meeus, "Astronomical Algorithms")
- Häuser: Placidus-System
- KI-Modell: Claude Sonnet 4 (Streaming)
- Keine externen Dependencies (außer Google Fonts)
- 100% clientseitig, keine Daten werden an Server gesendet (außer an Anthropic für die KI)
