# Spacewar 3D (Version 0.69)
Ein rundenbasiertes 3D-Strategiespiel im Weltraum, inspiriert von Klassikern wie *Risiko*.

## Beschreibung
Das Ziel ist die Eroberung aller Planeten der Galaxie. Du trittst gegen bis zu fünf KI-Gegner an. Das Spiel verfügt über anpassbare Regeln, diverse Zufallsereignisse und flexible Einstellungen für Schwierigkeitsgrad, Spielfläche und Medien.

## Technischer Stack
- Statisches Single-File-Projekt (HTML, CSS, JS inline in `index.html`)
- Kein Build-System, keine npm-Abhängigkeiten
- Three.js r128 & OrbitControls für 3D-Rendering
- Tailwind CSS für UI-Styling
- Alle Bibliotheken werden via CDN geladen
- Media-Dateien (`.mp3`, `.mp4`, `.png`) liegen flach im Projektroot

## Schnellstart
1. Projektdateien lokal verfügbar machen (Klonen oder Download)
2. Spiel starten:
   - Option A: `index.html` direkt im Browser öffnen
   - Option B: Lokalen HTTP-Server starten (empfohlen für korrektes Medien-Laden):
     ```bash
     python3 -m http.server 8000
     ```
     Danach `http://localhost:8000/index.html` im Browser aufrufen

## Features
- 1 menschlicher Spieler + bis zu 5 KI-Gegner
- Einstellbare Parameter: Spieleranzahl (2-6), Planetenzahl (15-50), Schwierigkeitsgrad
- Konfigurierbare KI (Aggressionslevel, Angriffsverhalten)
- Dynamische Zufallsereignisse (Sonnenstürme, Meteoritenschauer, Supernovae etc.)
- Medienanpassung: Hintergrundvideos, Musik, Sound-Sets und Vordergrund-Overlays wählbar
- Spielstände via `localStorage` speichern/laden

## Steuerung
- **Maus**: Linksklick auf Planeten für Aktionen, Rechtsklick zum Rotieren, Scrollen zum Zoomen
- Alle weiteren Aktionen über die In-Game UI-Steuerelemente
