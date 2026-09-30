# 🛡️ Anleitung: Cloudflare Worker als sicherer Gemini API Proxy

Durch diesen Proxy bleibt dein **Gemini API-Key absolut geheim** auf den Cloudflare-Servern gespeichert. Nutzer im Browser können den Key nicht auslesen oder missbrauchen.

---

## Schritt 1: Cloudflare Worker erstellen
1. Logge dich auf [cloudflare.com](https://www.cloudflare.com/) ein.
2. Gehe im linken Menü auf **Workers & Pages**.
3. Klicke auf **Create application** -> **Create Worker**.
4. Vergib einen Namen (z. B. `gemini-sar-proxy`) und klicke auf **Deploy**.

---

## Schritt 2: Code einfügen & Speichern
1. Klicke im neu erstellten Worker auf **Edit code**.
2. Ersetze den gesamten Inhalt durch den Code aus `worker.js`.
3. Klicke oben rechts auf **Save and deploy**.

---

## Schritt 3: Gemini API-Key als Secret hinterlegen
1. Navigiere in deinem Worker zu **Settings** -> **Variables and Secrets**.
2. Klicke unter **Secrets** auf **Add secret**.
3. **Variable name:** `GEMINI_API_KEY`
4. **Value:** Füge deinen echten Google Gemini API-Key ein (z. B. `AIzaSy...`).
5. Klicke auf **Save and deploy**.

---

## Schritt 4: Worker URL im Dashboard nutzen
Cloudflare erzeugt eine Proxy-URL für dich (z. B. `https://gemini-sar-proxy.dein-subdomain.workers.dev`). Trage diese URL ganz oben in `index.html` bei `CLOUDFLARE_WORKER_URL` ein, damit der **AI Mission Copilot** sicher kommunizieren kann!