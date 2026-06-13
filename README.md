# NWB KI Bildungs-Bot — Werbe-Website (Prototyp)

Statische Seiten, kein Build nötig — einfach hochladen.

## Struktur
```
nwb-ki-bot-website/
├─ index.html              ← Landingpage (Marketing)
├─ bot/
│  └─ index.html           ← Bot-Einstieg, leitet zum Prototyp weiter
└─ assets/
   ├─ nwb-logo.svg         ← NWB-Logo (Platzhalter, s. u.)
   └─ screenshots/         ← fach-tutor.png · dashboard.png · simulation.png
```

## Zwei Links zum Verschicken
- **Komplette Landingpage:**  `https://<deine-seite>/`
- **Nur der Bot:**            `https://<deine-seite>/bot/`  (kurze NWB-Splash-Seite → leitet weiter zum Bot)

Hinweis: Der Bot selbst läuft als eigene App unter `https://nwb-ki-bot.vercel.app`.
Diese Adresse kannst du ebenfalls direkt teilen – sie zeigt nur den Bot, ohne Landingpage.
Die `/bot/`-Seite ist nur die saubere Einstiegs-URL unter deiner eigenen Adresse.

## Auf GitHub veröffentlichen (Pages)
1. Ordnerinhalt ins Repo hochladen (`index.html` im Stammverzeichnis).
2. Settings → Pages → Source: Branch `main` / `/root` → Save.
3. Seite erscheint unter `https://<user>.github.io/<repo>/`, der Bot unter `.../bot/`.

## Weiterleitungsziel des Bots ändern
In `bot/index.html` die URL `https://nwb-ki-bot.vercel.app` an zwei Stellen anpassen
(`<meta http-equiv="refresh">` und die Variable `TARGET` im Script).

## Echte Unterseite unter EINER Domain (optional, sauberste Lösung)
Wenn Landingpage und Bot unter derselben Domain liegen sollen (`/` = Landingpage, `/bot` = Bot),
ist der beste Weg, beides in DAS Vercel-Projekt des Bots zu legen:
- Landingpage als Startroute (`app/page.tsx` bzw. statisch im `public/`-Root)
- den bisherigen Bot auf die Route `/bot` verschieben
Dann teilst du `…/` für die Landingpage und `…/bot` für den Bot – ohne Weiterleitung.

## Logo
`assets/nwb-logo.svg` ist DEIN Logo-Slot. Lade dort das offizielle NWB-Logo hoch (gleicher
Dateiname `nwb-logo.svg`). Diese Datei ist NICHT Teil der ZIPs — sie wird beim Hochladen der
Website-Updates also nie überschrieben. Falls `nwb-logo.svg` fehlt, zeigt die Seite automatisch
das mitgelieferte Platzhalter-Logo `assets/nwb-logo-fallback.svg`.

Das offizielle, frei lizenzierte Original-SVG liegt bei Wikimedia Commons (File:NWB-Verlag-Logo.svg):
„Originaldatei" herunterladen, in `nwb-logo.svg` umbenennen, nach `assets/` hochladen.


## Screenshots einfügen
PNGs (~1200 px breit, 16:10) unter `assets/screenshots/` ablegen:
`fach-tutor.png`, `dashboard.png`, `simulation.png`. Fehlt eine Datei, zeigt der Platz einen Platzhalter.
