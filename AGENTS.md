# AGENTS.md - Spacewar 3D

## Projektart
Statisches Single-File HTML/JS-Spiel (Three.js, Tailwind CSS via CDN). Kein Build-System, keine npm-Abhängigkeiten.

## Ausführen
```bash
# Einfach die index.html im Browser öffnen oder via HTTP-Server bereitstellen:
python3 -m http.server 8000
# Dann http://localhost:8000/index.html aufrufen
```

## Code-Struktur
- `index.html` enthält gesamten Code (HTML, CSS, JS inline)
- Media-Dateien (`.mp3`, `.mp4`, `.png`) liegen flach im Root-Verzeichnis
- Three.js r128, OrbitControls und Tailwind CSS werden per CDN geladen

## Wichtige Konstanten (in index.html)
- `KI_CONFIG` (Zeile ~298): KI-Verhalten, Gewinnchancen, Aggressionslevel
- `GAME_RULES` (Zeile ~307): Planeten-Bonus-Regeln
- `EVENTS_CONFIG` (Zeile ~312): Zufallsereignisse und Gewichtung

## Besonderheiten
- Keine Tests vorhanden
- Kein Linting/Formatierung konfiguriert
- Spielstände werden im localStorage gespeichert (`save-game-btn`)
- Sound-System wählt Dateien basierend auf `currentSoundSetIndex` (`angriff01.mp3` bis `angriff09.mp3`)
