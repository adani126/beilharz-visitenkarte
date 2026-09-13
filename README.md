# Digitale Beilharz-Visitenkarte

Die Seite ist eine reine statische Website und wird kostenlos über GitHub Pages bereitgestellt: **https://adani126.github.io/beilharz-visitenkarte/**

Alle sichtbaren Angaben (Name, Position, Kontakt, Standorte, Firmenlogo) sind echter Text bzw. austauschbare Bilddateien – nichts davon ist mehr in ein Bild "eingebrannt". Änderungen lassen sich direkt im Browser über GitHub vornehmen, ganz ohne Programmierkenntnisse.

## Etwas ändern

1. Gehe zur Datei `index.html` im Repository.
2. Klicke oben rechts auf das Stift-Symbol ("Edit this file").
3. Suche die passende Stelle (siehe Übersicht unten) und ändere den Text.
4. Unten auf "Commit changes" klicken – nach ca. 1 Minute ist die Änderung live.

Übersicht, wo was steht (Kommentare `<!-- ... -->` in `index.html` markieren die Abschnitte zusätzlich):

| Was | Wo in `index.html` |
|---|---|
| Name | `<h1 class="name">André Daniel</h1>` |
| Positionen | `<ul class="positions">` – jede Position eine eigene `<li>`-Zeile |
| Firmenname | `<h2 class="org">` |
| Adresse, Telefon, Fax, Website | Abschnitt "KONTAKTKARTE" |
| Reparaturannahme / Ersatzteillager | Abschnitt "REPARATURANNAHME / ERSATZTEILLAGER" |
| Standorte (Duisburg, Essen, Gelsenkirchen, …) | Abschnitt "UNSERE STANDORTE" – ein Standort hinzufügen/entfernen = einen `<li>`-Block kopieren, anpassen oder löschen |
| Leistungen | Abschnitt "UNSERE LEISTUNGEN" |
| Impressum/Datenschutz-Links, Copyright-Jahr | `<footer class="site-footer">` |

**Telefonnummern/Links:** Bei `tel:`- und `mailto:`-Links (z. B. `href="tel:+492065996513"`) muss die Nummer sowohl im sichtbaren Text als auch im `href` angepasst werden.

## Firmenlogo austauschen

Das Logo (`assets/beilharz-logo.png`) ist eine eigene, freigestellte Bilddatei – unabhängig vom Werkstattfoto. Es enthält **kein** "125 Jahre"-Jubiläumszeichen mehr; dieser Zusatz steht als normaler Text direkt über dem Logo (`<p class="anniversary">125 Jahre</p>`) und kann jederzeit gelöscht oder geändert werden, sobald das Jubiläumsjahr vorbei ist.

Um das Logo komplett auszutauschen: neue Datei unter demselben Namen `assets/beilharz-logo.png` hochladen (im Ordner `assets` → "Add file" → "Upload files"). Am besten ein Logo mit transparentem Hintergrund (PNG) verwenden, damit es sich nahtlos in das Foto einfügt.

## Werkstattfoto austauschen

Das Hintergrundfoto liegt als `assets/hero.jpg` vor. Es kann durch ein neues Foto im selben Format ersetzt werden (gleicher Dateiname). Für ein stimmiges Ergebnis sollte das neue Foto ein ähnliches Seitenverhältnis wie das aktuelle (ca. 916 × 483 Pixel) haben und im oberen linken Bereich genug Platz für das Logo lassen.

## vCard-Kontakt anpassen

Für den "Kontakt speichern"-Button ist zusätzlich `andre-daniel.vcf` anzupassen (auf CRLF-Zeilenenden achten).

## Veröffentlichung mit GitHub Pages

Ist bereits eingerichtet (Branch `main`, Ordner `/root`). Bei neuen Commits auf `main` aktualisiert sich die Seite automatisch nach ca. 1 Minute – ganz ohne weitere Schritte.

## NFC-Karte

Die NFC-Karte (NTAG216) enthält nur die URL `https://adani126.github.io/beilharz-visitenkarte/` als URL-Datensatz. Sie muss **nicht** neu beschrieben werden, wenn sich Inhalte auf der Seite ändern – nur falls sich die URL selbst ändert.
