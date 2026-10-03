# Maze of Life — Generative Art

> A seed-based generative system for cellular-automata compositions.  
> A reproducible catalogue of computational life studies.

---

## What is this?

**Maze of Life** is a generative design system built on cellular automata — grids of cells that evolve according to simple neighbourhood rules. Each seed initializes a grid of 100 to 200 columns by 100 to 200 rows, applies a Conway-style rule for 500 to 10,500 generations, and settles into a maze of colour and void.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the sense of labyrinthine structure that emerges from simple rules repeated many times, **Maze of Life** reframes cellular evolution as a textile.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Maze-of-Life/)**

---

## The System

The generator is a single-layer system — a grid of living cells evolving through time:

| Layer | Description |
|-------|-------------|
| **Grid** | 100–200 columns × 100–200 rows, initialized at 40–90% density. |
| **Evolution** | A Conway-style rule applied for 500–10,500 generations, until the grid settles. |
| **Colour** | Each surviving cell is tinted from a shared foreground palette. |

All layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Grid dimensions** — 100 to 200 columns × 100 to 200 rows
- **Total cells** — 10,000 to 40,000
- **Initial density** — 40% to 90% live cells
- **Iterations** — 500 to 10,500 generations
- **Neighbourhood rule** — Conway-style (survive at 2–3, revive at 3)
- **Background** — drawn from 27 curated dark tones
- **Foreground palette** — drawn from 44 curated colour sets (2–8 colours each)

---

## Structure

```
Maze-of-Life/
├── index.html              ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── maze-tote.png
│   ├── maze-cushion.png
│   └── ...
├── Maze-of-Life.jpg        ← Apparel mockup
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no dependencies, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Live catalogue** — cover, statement, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Color System

Every composition is drawn from two curated palettes:

- **Background** — one of 27 dark tones (blacks, deep blues, teals, muted reds, charcoals) chosen per seed
- **Foreground** — one of 44 curated sets, each containing 2 to 8 harmonious or contrasting colours

Each surviving cell in the final grid picks its fill colour at random from the foreground set. Because both the evolution and the colours are seeded, no two compositions share the same rhythm of maze and hue.

---

## Technical Notes

- Pure vanilla JavaScript — no libraries
- Canvas 2D rendering
- Custom xorshift random generator for deterministic seeds
- Device-pixel-ratio aware rendering
- Fully static rendering — one seed produces one composition, no animation loops
- Single `renderStatic()` function drives the cover, plate, framed print, all four surfaces, and all eight archive thumbnails
- Conway-style neighbourhood rules (survive at 2–3 neighbours, revive at exactly 3)
- In-place matrix evolution for performance
- **Performance note** — this is the heaviest of the six systems. A single composition can involve up to 420 million rule applications (10,500 iterations × 40,000 cells). On slower devices, the initial render may take a few seconds.
- `prefers-reduced-motion` respected

---

## About

**Maze of Life** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Maze of Life** is an attempt to render that logic visible.

> *Every cell is a small decision — and every decision rewrites the one after it.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Maze of Life — Autumn 2026

---

<p align="center">
  <em>Generative Cellular Automata</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>