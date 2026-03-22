# CSS-Struktur

Diese Ordnerstruktur trennt Basis-, Bereichs- und Mobile-Styles klar, damit Änderungen leichter zu finden und zu debuggen sind.

## Struktur
- `base.css`: Root-Variablen, Reset, globale HTML/Body-Regeln
- `utilities.css`: Container, Section, Divider, Hilfsklassen
- `buttons.css`: Button-Stile (`.btn*`)
- `animations.css`: Animationen (`.fade-in*`)

- `header.css`, `hero.css`, `services.css`, `about.css`, `stats.css`, `projects.css`, `contact.css`, `footer.css`
  Bereichsbezogene Styles für die jeweiligen Sektionen

- `mobil/`
  Mobile Overrides pro Bereich (nur Media Queries)
  - `header.css`
  - `hero.css`
  - `services.css`
  - `about.css`
  - `contact.css`

## Reihenfolge in `index.html`
1. Base + Utilities + Buttons + Animations
2. Bereichs-Dateien (Header → Footer)
3. Mobile-Dateien (alle `mobil/*.css` am Ende)

So überschreiben Mobile-Dateien die Desktop-Styles gezielt und nachvollziehbar.
