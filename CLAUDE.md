# Tagesheim Oberstufe – Auslieferungs-Repo (GitHub Pages)

Dieses Repo liefert nur die fertige, **passwortverschlüsselte** Dienstplan-Seite aus: https://dendak.github.io/tagesheim-oberstufe/
Kein Quellcode hier. Quellprojekt: privates Repo `Dendak/tagesheim-projekt` (lokal `C:\Users\holub\code\tagesheim-projekt`), Details in dessen CLAUDE.md.
Die Hauptversion läuft inzwischen auf https://tagesheim.herzjesugym.com (Microsoft-Anmeldung); diese Passwort-Version bleibt laut Denis vorerst online.

## Struktur
- `index.html` – die komplette Seite, Schülerdaten AES-256-GCM-verschlüsselt eingebettet (PBKDF2-SHA-256, 600 000 Iterationen).
- `README.md` – Kurzbeschreibung für Besucher:innen des Repos.
- `app-test.html` – Testseite für Untis-App-Links, ohne Daten (laut Commit „wird wieder entfernt").

## Aktualisieren und Deployment
- Nie direkt hier editieren. Änderungen im Quellprojekt machen, dort bauen, das Ergebnis als `index.html` hierher kopieren.
- Achtung (Stand 07.10.2026): Der aktuelle `build.py` im Quellprojekt erzeugt **kein** verschlüsseltes `dist/index.html` mehr,
  sondern nur `dist/easyname/` (Microsoft-Anmeldung, ohne Daten) und `dist/lokal.html` (Klartext!). Beides gehört **nicht** hierher.
  Vor einem Update klären, wie die verschlüsselte Variante gebaut werden soll.
- Jeder Push auf `main` ist sofort live (GitHub Pages, Branch `main`, Ordner `/ (root)`).

## Vorsicht – Datenschutz (nicht verhandelbar)
- Die Seite betrifft 334 minderjährige Schüler:innen. Das Repo ist **öffentlich**.
- `index.html` darf keinen einzigen Klarnamen enthalten. Nie Excel-Listen, `rows.json`, `dist/lokal.html` o. Ä. hierher legen.
- Die Git-Historie behält alles – ein einmal gepushter Klarname ist nicht mehr sauber zu entfernen.
- Vor jedem Commit die Leck-Prüfung aus tagesheim-projekt/CLAUDE.md („Datenschutz") ausführen: Kontrollnamen-Suche in `index.html` muss 0 ergeben.
  Gründlicher ist die Ganzwort-Prüfung gegen alle Namen, wie sie `build.py` macht.
- Das Passwort steht nirgends im Repo und kommt auch nie hinein (auch nicht in Commit-Texte oder Notizen).

## Arbeit über mehrere Geräte
- GitHub ist die Quelle der Wahrheit. Lokal liegt das Repo unter `C:\Users\holub\code\tagesheim-oberstufe` – nie in OneDrive.
- Session-Start: `git pull`, dann diese CLAUDE.md und [docs/POZNAMKY.md](docs/POZNAMKY.md) lesen.
- Session-Ende: POZNAMKY.md aktualisieren (Verlauf, offene Punkte), committen, pushen (nach der Leck-Prüfung).
- Riskante Änderungen (alles an `index.html`, Löschen der Seite) über Branch + Pull Request, nicht direkt auf `main`.
