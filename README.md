# Restkraftstoff

Restkraftstoff-Rechner für das Segelboot. Er läuft komplett offline auf dem Handy.

- **Rechner:** Tankinhalt bei Abfahrt minus Motorfahrten (Dauer × Verbrauch nach Drehzahl). Angezeigt werden die Restmenge, der Tank-Füllstand, die Laufzeit bis zur Reserve bzw. bis leer und eine Reichweitentabelle je Drehzahl.
- **Boot:** Tankgröße, Reserve in %, nicht ansaugbare Restmenge und die Verbrauchstabelle Drehzahl → l/h. Zwischenwerte werden linear gerechnet.
- Alle Daten bleiben im Browser des Geräts (`localStorage`). Es gibt keinen Server und kein Konto.

## Aufs iPhone bringen

1. Die Seite einmal mit Internet in **Safari** öffnen.
2. Teilen → **„Zum Home-Bildschirm"**.
3. Danach startet die App vom Home-Bildschirm aus, auch ohne Netz.

## Hosting (GitHub Pages)

Settings → Pages → *Deploy from a branch* → `main` / `/ (root)`.
Die App nutzt nur relative Pfade und läuft deshalb auch unter `https://<user>.github.io/restkraftstoff/`.

## Updates

Nach einer Änderung an den Dateien in `sw.js` die `VERSION` hochzählen. Das Handy holt sich die neue Version beim nächsten Start mit Netz und zeigt sie ab dem übernächsten Start.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette App (HTML, CSS, JS) |
| `sw.js` | Service Worker: speichert alle Dateien für den Offline-Betrieb |
| `manifest.webmanifest` | App-Name, Icon, Vollbild-Start |
| `icons/` | App-Icons (`icon.svg` ist die Vorlage) |
