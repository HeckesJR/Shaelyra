[README.md](https://github.com/user-attachments/files/33381327/README.md)
# Shaelyra – Spielbegleiter

DSA 4.1 für Shaelyra Firnwind. Eine Web-App ohne Server, läuft offline.

Tabs: Status, Proben, Zauber, Kampf, Reise, Regeln, Mehr (Steigern, Würfe, Charakter & Sicherung).

## Was ins Repository gehört (öffentlich)

Nur diese vier Dateien hochladen:

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icon.svg`

**Nicht** hochladen: die Ordner `build` und `privat`. Der Ordner `privat` enthält Text aus den Regelbüchern und darf nicht öffentlich werden.

## Update einspielen

Auf GitHub im Repository `index.html` öffnen → Stift-Symbol / „Upload files" → die neue `index.html` hochladen → Commit.
Auf dem Handy die App schließen und neu öffnen (bei Bedarf einmal neu laden). Gespeicherte Werte bleiben erhalten.

## Regel-Suche einrichten (einmal pro Gerät)

1. Datei `privat/regeln_index.json.gz` aufs Handy bringen (z. B. per Cloud-Ordner oder Mail an dich selbst).
2. In der App: Tab **Regeln** → „Index-Datei auswählen" → die Datei wählen.
3. Danach funktioniert die Suche offline. Der Index bleibt nur auf diesem Gerät.

## Neu bauen (am PC)

- App: `node build/build.js` erzeugt `index.html` aus `build/template.html`, `part2.js` und den Zaubertexten.
- Charakterwerte stehen in `build/template.html` im Block `CHAR`.
- Regel-Index: `node build/build_rules.js` (braucht `pdftotext`).
- Lokal testen: `node build/serve.js`, dann http://localhost:5173 öffnen.
