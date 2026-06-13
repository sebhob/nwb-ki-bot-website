# Landingpage online stellen — Schritt für Schritt

Die Seite ist statisch (nur HTML/SVG). Du brauchst keinen Server und kein Build-Tool.
Drei Wege — wähle einen. Empfohlen: **A) GitHub Pages**, weil du GitHub schon nutzt.

---

## A) GitHub Pages (empfohlen)

1. ZIP entpacken. Du hast dann den Ordner `nwb-ki-bot-website/` mit:
   `index.html`, `bot/`, `assets/`.
2. Auf https://github.com einloggen → oben rechts **+** → **New repository**.
   - Name z. B. `nwb-ki-bot-website`
   - **Public**
   - KEIN Häkchen bei „Add a README"
   - **Create repository**
3. Auf der leeren Repo-Seite: Link **„uploading an existing file"** anklicken.
4. Den **Inhalt** des entpackten Ordners hineinziehen — also `index.html`, den Ordner `bot` und den Ordner `assets` (NICHT den äußeren Ordner selbst).
   `index.html` muss direkt im Wurzelverzeichnis liegen.
5. Unten **Commit changes**.
6. **Settings** (oben im Repo) → links **Pages**.
   - „Build and deployment" → Source: **Deploy from a branch**
   - Branch: **main**, Ordner: **/ (root)** → **Save**
7. Kurz warten (1–2 Min), Seite neu laden. Oben erscheint:
   `https://<dein-username>.github.io/nwb-ki-bot-website/`
   - Landingpage: diese URL
   - Nur-Bot-Einstieg: `…/nwb-ki-bot-website/bot/`

> Tipp: Lege dafür ein **eigenes** Repo an (nicht das Bot-Repo). So bleiben Website und Bot sauber getrennt.

---

## B) Netlify Drop (am schnellsten, ~30 Sekunden, ohne Account-Pflicht)

1. ZIP entpacken.
2. https://app.netlify.com/drop öffnen.
3. Den entpackten Ordner `nwb-ki-bot-website` ins Fenster ziehen.
4. Fertig — du bekommst sofort eine Live-URL (z. B. `https://random-name.netlify.app`).
   Umbenennen/eigene Domain geht später in den Site-Settings.

---

## C) Vercel (passt zum Bot-Hosting)

1. https://vercel.com → **Add New… → Project**.
2. Repo importieren (das GitHub-Repo aus Variante A) — Framework: **Other / kein Framework**.
3. **Deploy**. Vercel liefert eine `…vercel.app`-URL.

---

## Eigene Domain (optional)
Bei allen drei Anbietern lässt sich in den Projekt-/Site-Einstellungen eine eigene
(Sub-)Domain hinterlegen, z. B. `lernbot.nwb.de` — DNS-Eintrag laut Anbieter-Anleitung setzen.

## Bot-Link
Die „Prototyp öffnen"-Buttons führen direkt zu `https://nwb-ki-bot.vercel.app`.
Zum Ändern in `index.html` nach `nwb-ki-bot.vercel.app` suchen und ersetzen
(bzw. in `bot/index.html` für die Einstiegsseite).
