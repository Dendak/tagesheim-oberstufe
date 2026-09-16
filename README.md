# Tagesheim Oberstufe – Dienstplan

Webseite für die Lehrkräfte des Tagesheims Oberstufe am Privatgymnasium der Herz-Jesu-Missionare Salzburg.

- Namen auswählen und den eigenen Wochenplan sehen
- Auf eine Stunde tippen: Schüler:innen dieser Stunde, nach Klassen
- „Liste für …“: alle Schüler:innen eines Diensttags zum Übertragen in die WebUntis-Gruppe (inkl. LK/LL-Laborschüler:innen)

## Datenschutz

Die Schülerdaten sind in `index.html` **verschlüsselt** eingebettet (AES-256-GCM, Schlüssel per PBKDF2-SHA-256 mit 600.000 Durchläufen). Ohne Passwort ist nur verschlüsselter Text sichtbar. Das Passwort steht nirgends im Repository und wird nur im Kollegium weitergegeben.

Bitte keine unverschlüsselten Excel-Listen oder Versionen mit lesbaren Namen in dieses Repository legen. Achtung: Alles, was einmal committet wurde, bleibt in der Git-Historie.

Lehrkräfte können zusätzlich eine neuere Excel-Liste direkt auf der Seite öffnen; sie wird nur im eigenen Browser gelesen.

## Lesart der Liste

| Eintrag | Bedeutung |
|---|---|
| `1` | anwesend |
| `U` | Unterricht, nicht im Tagesheim |
| leer | nicht anwesend |
| `-6 BENH` (KV-Zeile) | 6 Schüler:innen der Klasse sind in dieser Stunde bei BENH eingeteilt |
| `LK` / `LL` | nur an den 12 Laborterminen angemeldet (LK = frühes Labor 13:30, LL = spätes Labor 16:00) |

## Veröffentlichen mit GitHub Pages

Settings → Pages → Branch `main`, Ordner `/ (root)` → Save.
