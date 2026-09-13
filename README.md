# Digitale Beilharz-Visitenkarte

Die Seite ist eine reine statische Website und kann direkt kostenlos über GitHub Pages bereitgestellt werden.

## Veröffentlichung mit GitHub Pages

1. Erstelle auf GitHub ein neues, leeres Repository, zum Beispiel `beilharz-visitenkarte`.
2. Lade **den gesamten Inhalt dieses Ordners** hoch (inklusive `assets`).
3. Öffne im Repository **Settings → Pages** und wähle bei *Branch* `main` sowie den Ordner `/(root)` aus.
4. GitHub zeigt anschließend die HTTPS-Adresse an, etwa `https://BENUTZERNAME.github.io/beilharz-visitenkarte/`.
5. Öffne diese Adresse auf einem Smartphone und teste alle sechs Schaltflächen sowie den vCard-Download.

## NFC-Karte schreiben

Erst nach dem erfolgreichen Test die endgültige HTTPS-Adresse in einer NFC-Schreib-App als **URL-Datensatz** auf den NTAG216 schreiben. Die Karte enthält dann nur die URL, daher können spätere Änderungen an der Website ohne erneutes Beschreiben der Karte erfolgen.

## Inhalt ändern

Kontaktdaten stehen in `index.html`; für den gespeicherten Kontakt zusätzlich `andre-daniel.vcf` anpassen (auf CRLF-Zeilenenden achten). Das sichtbare Kartenmotiv liegt als `assets/beilharz-visitenkarte-final.png` (Fallback) und `assets/beilharz-visitenkarte-final.webp` (wird bevorzugt geladen, deutlich kleiner) vor. Beim späteren Logo-/Design-Austausch beide Dateien unter demselben Namen ersetzen und – falls sich die Bildmaße ändern – die `width`/`height`-Attribute des `<img>` sowie die Prozentwerte der Schaltflächen in `styles.css` anpassen.

## Performance

Das Kartenmotiv wird als WebP (≈230 KB statt ≈1,8 MB als PNG) ausgeliefert; ältere Browser ohne WebP-Unterstützung erhalten automatisch die PNG-Fassung. Die Bilddatei wird zusätzlich per `<link rel="preload">` vorab geladen, damit die Karte auf dem Smartphone schnell sichtbar ist.

Die Dateien `assets/actros*.png`, `assets/iveco.jpg`, `assets/man-tgx.jpg` sowie `assets/beilharz-entwurf.png`, `assets/beilharz-confirmed.png`, `assets/beilharz-final.png` und `assets/beilharz-stand.png` sind frühere Entwurfsstände/Bildquellen und werden von `index.html` nicht mehr eingebunden. Sie können vor dem Hochladen zu GitHub entfernt werden, um das Repository klein zu halten – oder als Archiv behalten werden.
