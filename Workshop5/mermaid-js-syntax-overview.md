# Mermaid.js Syntax Kurzübersicht

Mermaid.js ist ein JavaScript-basiertes Diagramm- und Charting-Tool, das Markdown-inspirierte Textdefinitionen rendert, um Diagramme dynamisch zu erstellen.

## Grundstruktur

```
graph [Richtung]
    [Knotendefinitionen]
    [Verbindungsdefinitionen]
```

## Diagrammtypen

1. Flussdiagramm: `graph` oder `flowchart`
2. Sequenzdiagramm: `sequenceDiagram`
3. Klassendiagramm: `classDiagram`
4. Zustandsdiagramm: `stateDiagram-v2`
5. Entity-Relationship-Diagramm: `erDiagram`
6. User Journey: `journey`
7. Gantt-Diagramm: `gantt`
8. Kreisdiagramm: `pie`

## Flussdiagramm

### Knoten

- `id[Text]`: Rechteckiger Knoten
- `id(Text)`: Abgerundeter rechteckiger Knoten
- `id((Text))`: Kreisförmiger Knoten
- `id>Text]`: Asymmetrische Form
- `id{Text}`: Raute

### Verbindungen

- `A --> B`: Pfeil
- `A --- B`: Linie
- `A -.- B`: Gepunktete Linie
- `A ==> B`: Dicker Pfeil
- `A -- Text --> B`: Pfeil mit Text

### Richtungen

- TB: Top to bottom (Von oben nach unten)
- TD: Top-down (Von oben nach unten, gleich wie TB)
- BT: Bottom to top (Von unten nach oben)
- RL: Right to left (Von rechts nach links)
- LR: Left to right (Von links nach rechts)

## Sequenzdiagramm

```
sequenceDiagram
    participant A
    participant B
    A->>B: Nachricht
    B-->>A: Antwort
```

## Klassendiagramm

```
classDiagram
    Klasse01 <|-- EineSehrLangeKlasse : Vererbung
    Klasse03 *-- Klasse04 : Komposition
    Klasse05 o-- Klasse06 : Aggregation
```

## Zustandsdiagramm

```
stateDiagram-v2
    [*] --> Zustand1
    Zustand1 --> [*]
    Zustand1 : Beschreibung
    Zustand1 --> Zustand2 : Übergang
```

## Entity-Relationship-Diagramm

```
erDiagram
    KUNDE ||--o{ BESTELLUNG : platziert
    BESTELLUNG ||--|{ POSITION : enthält
```

## User Journey

```
journey
    title Meine Reise
    section Abschnitt 1
      Aufgabe 1: 5: Ich
      Aufgabe 2: 3: Ich, Katze
```

## Gantt-Diagramm

```
gantt
    title Projekt-Zeitplan
    dateFormat  YYYY-MM-DD
    section Abschnitt
    Aufgabe1        :a1, 2023-01-01, 30d
    Aufgabe2        :after a1, 20d
```

## Kreisdiagramm

```
pie
    title Schlüsselelemente in Produkt X
    "Kalzium" : 42.96
    "Kalium" : 50.05
    "Magnesium" : 10.01
    "Eisen" :  5
```

Diese Kurzübersicht deckt die grundlegende Syntax für verschiedene Diagrammtypen in Mermaid.js ab. Für detailliertere Informationen und fortgeschrittene Funktionen, konsultieren Sie bitte die offizielle Mermaid.js-Dokumentation.
