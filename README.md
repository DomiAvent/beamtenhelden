# Beamtenhelden Landingpage

Statische Landingpage für Beamtenhelden (Aventus Versicherungsmakler Augsburg AG). Läuft auf GitHub Pages ohne Build-Schritt.

## Struktur

```
.
├── index.html          # Die komplette Seite (HTML + CSS + JS inline)
├── images/
│   ├── vanessa.png     # Vanessa Eckstein
│   ├── thomas.png      # Thomas Kleinhappel
│   └── michael.png     # Michael Kleinhappel
└── README.md
```

## Auf GitHub Pages hosten

1. Neues GitHub-Repo anlegen, z.B. `beamtenhelden`
2. Alle Dateien (inkl. `images/`-Ordner) in das Repo hochladen
3. Im Repo: **Settings → Pages**
4. Bei **Source** „Deploy from a branch" wählen, Branch `main`, Ordner `/ (root)` → **Save**
5. Nach 1–2 Minuten ist die Seite unter `https://<dein-username>.github.io/beamtenhelden/` erreichbar

Bei Custom Domain: unter Settings → Pages eine Domain eintragen (z.B. `beamtenhelden.de`) und einen CNAME-Record beim Domain-Provider setzen.

## Microsoft Bookings Links eintragen

Im `index.html` nach `bookingUrl` suchen (4 Stellen):

- Vanessa: Zeile ~367 — individueller Link
- Thomas: Zeile ~378 — individueller Link
- Michael: Zeile ~389 — individueller Link
- Team: `id="team-booking"` im HTML oben — gemeinsamer Team-Link

Jede URL einmal ersetzen. Alle öffnen in neuem Tab.

## Kontaktdaten anpassen

Telefon, E-Mail, Adresse stehen im Footer (am Ende der Datei). Beim Aktualisieren auf beide Stellen achten:
- Footer-Kontaktblock
- FAQ-Sektion (E-Mail-Link bei „Deine Frage nicht dabei?")

## Bilder austauschen

Die drei PNG-Dateien in `images/` einfach überschreiben — gleicher Dateiname, gleiches Format (quadratisch, transparenter Hintergrund, 600×600 px empfohlen).

## Lokal testen

Einfach `index.html` im Browser öffnen — funktioniert direkt, keine Abhängigkeiten außer Internet (für Google Fonts + Tailwind CDN).

Falls du die Seite komplett offline testen willst: Browser kann Bilder aus einem lokalen Ordner laden, aber manche Browser erfordern einen lokalen Server. Einfachste Lösung:
```bash
cd <projekt-ordner>
python3 -m http.server 8000
# dann http://localhost:8000 aufrufen
```
