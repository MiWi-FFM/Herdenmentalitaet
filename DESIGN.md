# unser-plan.com — Designdefinition

Stand: 30.08.2026 · Gilt für Startseite und alle künftigen Planseiten
Maßgeblich sind die Referenzdateien des Skills `unser-plan-design`; dieses
Dokument fasst zusammen und hält die Begründungen fest.

---

## 1. Was die Seite ist

Private Sammelstelle für Reise- und Gruppenpläne. Startseite mit Kacheln,
dahinter je Plan eine passwortgeschützte Seite. Nicht öffentlich gelistet
(`noindex, nofollow`). Kein Teil der NMF-/chartroom-Markenwelt.

## 2. Marke

Geöffneter Ring, aus dem die Nadelspitze nach Nordosten ausbricht — Variante E4
mit Nadelform N2 (klassisch schlank), ausgewählt aus fünf Zeichenfamilien und je
sechs Varianten.

| Element | Wert |
|---|---|
| Ring | `circle r=22`, `dasharray 106 32`, `dashoffset -16`, `rotate(-52 32 32)` |
| Ringstärke | 3,4 in der Kachel · 4,0 flächenlos |
| Nadel | `M53 11 37.5 33.5 15 49Z` · zweite Hälfte `M53 11 30.5 26.5 15 49Z` bei 0,55 |
| Kachel | `rect 64×64 rx=14` |

Kleinfassung für 16/32 px als eigene Zeichnung: Ringstärke 5,4, `dasharray
98.2 40`, `dashoffset -20`, Eckradius 12, zweite Hälfte 0,35.

Ausführungen: Kachel schwarz (Hauptausführung), Weiß flächenlos, Grau 6E,
Schwarz flächenlos. Ohne Kachel wird die Nadel zur gefüllten Fläche — die
Zeichnung bleibt, die Polarität dreht. Kontrastuntergrenze 3:1.

Wortmarke: `unser` (300) · gepunktete Linie als Bindestrich · `plan` (800) ·
`.com` (500, 42 %, Deckkraft 0,55), Bricolage Grotesque, Laufweite −0,02 em.
Bleibt echter Text.

## 3. Oberfläche

Schwarz mit zwei Glasstufen, kein Farbton. Grund `#070707`, Verlauf nach
`#1C1C1C`, Korn bei 5 % gegen Farbringe, Unschärfe 26 px (18 px auf dem
Telefon). Vollständige Token in `references/oberflaeche.md`.

Pflichtrückfälle: `prefers-reduced-transparency`, `prefers-contrast: more`,
fehlendes `backdrop-filter`, `prefers-reduced-motion`.

## 4. Startseite

Kacheln in bis zu drei Bereichen: **Aktuell**, **In Planung**, **Abgeschlossen**.
Leere Bereiche werden nicht ausgegeben; Bereichsüberschriften erst ab zwei
belegten Bereichen.

**Vor dem Passwort stehen keine Details** — kein Datum, keine Orte, keine
Personenzahl. Erlaubt sind Name, Zustandsmarke, Sprachkürzel und die
Aufforderung.

Sprachkürzel: `rgba(245,245,245,.82)` auf `rgba(10,10,10,.5)`, Rahmen
`rgba(255,255,255,.24)`, 11 px halbfett — rund 11,5:1.

## 5. Planlogos

Vorlage: 1024 × 1024 px PNG mit transparentem Hintergrund. Daraus abgeleitet
512/256/128 als PNG und WebP unter `assets/plaene/<plan>/`.

In der Kachel als Wasserzeichen: 54 % der Kachelbreite (nicht in Pixeln),
rechts −8 %, unten −14 %, aufhellend überlagert (`mix-blend-mode: screen`) bei
0,72 Deckkraft, radial ausmaskiert. Text endet bei 72 % der Breite.

Auf der Planseite dagegen scharf und voll deckend im Kopf, 34–40 px, daneben
optional die Flagge (Region schlägt Land).

Pläne ohne Logo bekommen ein Monogramm.

## 6. Entscheidungen und ihre Gründe

| Entscheidung | Grund |
|---|---|
| Kein Glaseffekt in der Marke | Glas braucht etwas dahinter; bei 16 px, im Druck und in Vorschaubildern gibt es das nicht |
| Kachel als Hauptausführung | Eine weiße Nadel braucht eine Fläche, aus der sie geschnitten ist; zugleich fertiges App-Icon |
| Eigene Zeichnung für 16/32 px | Skalieren allein lässt die feine Fassung zulaufen |
| Wortmarke als Text | Schärfe, Vorlesbarkeit; Schriftdatei für Pfade liegt nicht vor |
| Schwarz statt Blau/Kupfer | Violett-Verlauf und NMF-Navy/Kupfer geprüft; Navy/Kupfer wirkt für eine private Reiseseite zu förmlich |
| Keine Details vor dem Passwort | ausdrückliche Entscheidung, 30.08.2026 |
| Wasserzeichen aufhellend überlagert | Dunkles Logo auf dunklem Glas bleibt sonst blass; Deckkraft allein holt nur einen farbigen Fleck nach vorn |
| Wasserzeichen in Prozent | feste Pixelmaße kollidierten bei schmaler Kachel und langem Namen |
| Sprachkürzel kräftiger | die frühere Fassung lag bei 3,9:1 und damit unter der Textgrenze von 4,5:1 |

## 7. Dateien

```
/                            index.html
/assets/logo/                Dachmarke: 5 SVG, 4 PNG
/assets/plaene/andalusien/   logo-1024/512/256/128.png + WebP
/assets/plaene/bootcamp/     bootcamp-1024/512/256/128.png + WebP
```

## 8. Offen

- Kachel für das AI-Bootcamp-Projekt: Name und Bereich stehen noch nicht fest,
  das Logo liegt aufbereitet bereit
- Zweite Sprache/weitere Pläne: Struktur steht, Inhalte fehlen
- Wortmarke in Pfade legen, falls eine Druckanwendung ansteht
- Der bestehende Andalusien-Reiseplan behält sein gewachsenes Layout, bis
  ausdrücklich etwas anderes entschieden wird
