# Gravitations-Simulation · Satellit um die Erde

Interaktive HTML-Simulation einer Satellitenbahn nach Newtonscher Gravitation.
Konzipiert für den Physikunterricht der **Klasse 10 (Gymnasium MV)** zur
Veranschaulichung der **1., 2. und 3. kosmischen Geschwindigkeit**.

Einzeldatei, keine Installation, läuft offline im Browser.

➡️ **Live:** _(nach Aktivierung von GitHub Pages hier eintragen)_
`https://DEIN-NAME.github.io/gravitation-simulation/`

---

## Was die Simulation zeigt

- **Kreisbahn** bei v = v₁ (1. kosmische Geschwindigkeit ≈ 7,91 km/s)
- **Elliptische Bahnen** bei v₁ < v < v₂
- **Parabolische Flucht** bei v = v₂ (2. kosmische Geschwindigkeit ≈ 11,19 km/s)
- **Hyperbolische Flucht** bei v > v₂ und insbesondere v ≥ v₃ (≈ 16,65 km/s)
- **Absturz** auf den Zentralkörper bei zu kleinem oder ungünstig gerichtetem v

Die Bahnart wird live klassifiziert und farblich markiert
(grün = gebunden, orange = Fluchtgrenze, rot = ungebunden).

## Bedienung

### Eingaben
| Element | Funktion |
|---|---|
| Startposition · Höhe | Höhe über dem Boden des Zentralkörpers in km |
| Geschwindigkeit · \|v\| | Betrag in m/s, frei wählbar |
| Geschwindigkeit · Winkel | 0° = tangential zur Kreisbahn, positiv = nach außen gekippt |
| Zentralkörper-Masse | Frei in kg eintippen (z. B. `5.972e24`) oder Preset wählen |
| v-Preset-Buttons | Setzen v automatisch passend zur aktuellen Höhe |

### Direkt im Bild
- **Geschwindigkeits-Pfeil ziehen** — Pfeilspitze anfassen → setzt |v| und Richtung
- **Satellit verschieben** — den gelben Punkt direkt im Bild ziehen
- **Mausrad** — zoomen

### Tastenkürzel
| Taste | Aktion |
|---|---|
| Leertaste | Start / Pause |
| R | Zurücksetzen auf Startzustand |
| 1 / 2 / 3 | 1./2./3. kosmische Geschwindigkeit setzen |

### HUD (oben links)
Live-Anzeige von |v|, Abstand r, Höhe h über Boden, Exzentrizität ε und Bahntyp.

## Physik

- **Newtonsche Gravitation:** F = G · m₁ · m₂ / r²
- **Numerische Integration:** Velocity-Verlet (symplektisch → energie­erhaltend,
  Bahnen leiern auch über viele Umläufe nicht aus)
- **Adaptive Schrittweite:** Δt ≤ T_Orbit / 2000, automatisch begrenzt
- **Bahnklassifikation** über spezifische Bahnenergie E und Exzentrizität
  ε = √(1 + 2EL² / (GM)²)

Verifiziert: Eine volle Erdumrundung bei v = v₁ liefert eine Abweichung
von < 0,0001 % im Bahnradius.

## Voreingestellte Zentralkörper

| Körper | Masse [kg] | Radius [km] |
|---|---|---|
| Mond    | 7,342 · 10²² | 1 737 |
| Erde    | 5,972 · 10²⁴ | 6 371 |
| Mars    | 6,39 · 10²³  | 3 389 |
| Jupiter | 1,898 · 10²⁷ | 69 911 |
| Sonne   | 1,989 · 10³⁰ | 695 700 |
| Uranus  | 8,681 · 10²⁵ | 25 362 |

Jeder Körper hat eine eigene Darstellung (Kontinente, Krater, Wolkenbänder etc.)
und eine **dünne Konturlinie am exakten Oberflächenradius** —
genau dort, wo v₁ und v₂ physikalisch definiert sind.

## Didaktische Einsatzmöglichkeiten

- **Einführung Kreisbahn:** Preset „1. kosm." → Kreisbahn beobachten,
  dann v leicht erhöhen/senken → Ellipse / Absturz
- **Fluchtgeschwindigkeit:** Stufenweise von v₁ über 1,2·v₁, 1,3·v₁ … bis v₂
  hochregeln und die Apoapsis beobachten — sie wächst gegen Unendlich
- **Massenabhängigkeit:** Preset Mond / Mars wählen — wie ändert sich v₁?
  (Schüler:innen vorhersagen lassen, dann verifizieren)
- **Drittes keplersches Gesetz:** Mit Zeitraffer mehrere Bahnen mit
  unterschiedlichem r vermessen
- **Vektorcharakter der Geschwindigkeit:** Winkel ≠ 0 → Ellipse mit
  versetzter Apsidenlinie; visualisiert direkt, dass v ein Vektor ist
  (Anschluss an „Kraft als vektorielle Größe")

## Bekannte Vereinfachungen

- Nur **zwei Körper** (Zentralkörper + Satellit, Satellit als Testteilchen)
- Keine Atmosphäre, keine Strahlung, kein Strahlungsdruck
- **3. kosmische Geschwindigkeit** ist nur als Zahlenwert hinterlegt
  (echte Demonstration bräuchte das volle Sonne-Erde-Satellit-System)
- 2D-Bewegung in der Bahnebene

## Lizenz / Nutzung

Freie Verwendung für Unterrichtszwecke. Über einen Hinweis bei Weitergabe
freue ich mich, ist aber nicht erforderlich.

---

_Erstellt mit Hilfe von Claude (Anthropic)._
