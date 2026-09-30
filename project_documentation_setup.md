# 🌙 Dancing with SARS — Lunar SAR & CLPS Landing Control Dashboard

**NASA Space Apps Challenge 2026**  
**Team:** `00000000A_LAGRANGE_NEXUS`  

Dieses Repository enthält genau die **6 essenziellen Dateien**, die du für den reibungslosen Betrieb und die Präsentation deines Lunar-Control-Center-Projekts benötigst.

---

## 📂 Die 6 notwendigen Projektdateien

1. **`index.html`** — Das interaktive Kontrollzentrum (Single-File Dashboard mit Leaflet-GIS, NASA LROC-Kacheln, Three.js 3D-Mond und Gemini AI Copilot).
2. **`generate_data.py`** — Die Python-Datenpipeline zur Berechnung von Kraterkoordinaten, PSR-Eisdepots und Gefahrenzonen.
3. **`data.json`** — Der strukturierte Datensatz im GeoJSON-Format.
4. **`worker.js`** — Das serverlose Edge-Skript für den sicheren Cloudflare Worker API-Proxy (schützt deinen Gemini API-Key).
5. **`worker_script_anleitung.md`** — Die Schritt-für-Schritt-Anleitung zur Einrichtung des Cloudflare Workers.
6. **`README.md`** — Diese vollständige Dokumentation inkl. Installationsanleitung.

---

## 🚀 Installations- und Einrichtungsanleitung

### Schritt 1: Python-Datenpipeline ausführen (optional falls data.json neu generiert werden soll)
```bash
python3 generate_data.py
```
Dies generiert die kompakte `data.json` mit allen Landezielen.

### Schritt 2: Dashboard starten
Öffne die Datei `index.html` direkt in deinem Webbrowser oder nutze einen lokalen Live-Server. 

### Schritt 3: Cloudflare Worker einrichten
Folge den Schritten in der Datei `worker_script_anleitung.md`, um den Cloudflare Worker einzurichten und trage deine URL direkt oben im JavaScript-Teil der `index.html` ein (`CLOUDFLARE_WORKER_URL`).