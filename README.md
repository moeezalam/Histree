<div align="center">

# Histree

### Watch the history of the world, in order.

**A cinematic curriculum for human civilization — every major empire, broken into historical phases, with the films, series, miniseries and documentaries that cover each phase, in the order you should watch them.**

[**→ Open the live atlas**](https://moeezalam.github.io/Histree/)

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://moeezalam.github.io/Histree/)
[![Empires](https://img.shields.io/badge/empires-15-c9a84c)](#the-empires)
[![Titles curated](https://img.shields.io/badge/titles%20curated-247-8b1a1a)](#the-empires)
[![No build step](https://img.shields.io/badge/build-none%20required-blue)](#run-it-locally)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-purple)](#contributing)

</div>

---

## The question this answers

> *"If I wanted to learn the entire history of Rome — or Egypt, or the Ottomans — through only film and television, in the right order, what would I watch?"*

No streaming guide, Wikipedia article, or YouTube list answers that properly. Histree does, for every civilization with enough screen coverage to make it possible.

It is a **two-level tree**:

- **Level 1 — the hub** ([`index.html`](index.html)): every empire as a node on a single visual tree. Solid lines are the main succession trunk and its forks; dashed lines are concurrent civilizations running elsewhere on the planet at the same time.
- **Level 2 — the empire timelines** ([`rome.html`](rome.html), [`egypt.html`](egypt.html), …): one file per empire. A vertical alternating timeline from founding to fall — each phase carrying its films, character spotlights, watch-order notes and parallel-viewing instructions.

Currently **15 empires · 110 historical phases · 247 curated titles**, spanning **1550 BC → 1997 AD**.

## The empires

| Empire | Span | Phases | Titles |
|---|---|--:|--:|
| [Roman Empire](https://moeezalam.github.io/Histree/rome.html) | 753 BC – 1453 AD | 22 | 77 |
| [Egyptian Empire](https://moeezalam.github.io/Histree/egypt.html) | c. 1550 – 30 BC | 8 | 28 |
| [Han Dynasty](https://moeezalam.github.io/Histree/han.html) | 206 BC – 220 AD | 10 | 16 |
| [Achaemenid Persia](https://moeezalam.github.io/Histree/persia.html) | 550 – 330 BC | 6 | 14 |
| [Maurya Empire](https://moeezalam.github.io/Histree/maurya.html) | 322 – 185 BC | 7 | 13 |
| [Islamic Caliphates](https://moeezalam.github.io/Histree/islamic.html) | 610 – 1258 AD | 7 | 12 |
| [Macedonian Empire](https://moeezalam.github.io/Histree/macedon.html) | 359 – 323 BC | 5 | 12 |
| [British Empire](https://moeezalam.github.io/Histree/british.html) | 1583 – 1997 AD | 7 | 11 |
| [Mughal Empire](https://moeezalam.github.io/Histree/mughal.html) | 1526 – 1857 AD | 7 | 11 |
| [Spanish Empire](https://moeezalam.github.io/Histree/spanish.html) | 1492 – 1975 AD | 7 | 10 |
| [Viking Age](https://moeezalam.github.io/Histree/viking.html) | 793 – 1066 AD | 4 | 10 |
| [Mongol Empire](https://moeezalam.github.io/Histree/mongol.html) | 1206 – 1368 AD | 5 | 9 |
| [Napoleon's Empire](https://moeezalam.github.io/Histree/napoleon.html) | 1799 – 1815 AD | 5 | 8 |
| [Ottoman Empire](https://moeezalam.github.io/Histree/ottoman.html) | 1299 – 1922 AD | 6 | 8 |
| [Japanese Imperial Age](https://moeezalam.github.io/Histree/japanese.html) | 1868 – 1945 AD | 4 | 8 |

**Not built yet — open for contributors:** Byzantine Empire (476–1453 AD) and Russian Empire (1721–1917 AD) already have nodes on the hub tree but no timeline file behind them. See [Contributing](#contributing).

## How to read a timeline

Every title carries a media-type badge, so you always know what you are committing to:

| Badge | Meaning |
|---|---|
| `FILM` | Feature film |
| `SERIES` | TV series |
| `MINI` | Miniseries |
| `DOC` | Documentary |
| `DRAMA` | Docudrama |
| ⟡ | Parallel / optional — safe to skip, or watch alongside |
| ◈ | Character spotlight — the people this phase belongs to |

Phases run top to bottom in chronological order. Read the phase description first, then watch its titles in the listed order.

## How it works

There is no framework, no bundler, no dependency tree, and no server.

- Every page is **one self-contained `.html` file** — markup, CSS and content in the same document.
- The only external request is the Google Fonts stylesheet (Cinzel + Cormorant Garamond).
- Pages link to each other with plain relative hrefs, so the whole thing works from `file://`, from GitHub Pages, or from any static host you drop it on.
- The visual language is fixed across the collection — dark marble, serif type, alternating left-right tree. **Only one thing changes per empire: the accent colour ramp.** Egypt is turquoise and sand, Persia is amethyst and gold, Rome is crimson. The unity is deliberate: the whole thing should read like one hand-made historical atlas.

The full design and research specification lives in [`PROJECT_BIBLE.html`](PROJECT_BIBLE.html) — CSS contract, phase anatomy, media-verification rules, and boilerplate templates. Open it in a browser before contributing.

## Run it locally

```bash
git clone https://github.com/moeezalam/Histree.git
```

Then open `index.html` in any browser. That's the whole setup.

Prefer a local server (optional):

```bash
python -m http.server 8000
```

## Contributing

Contributions are genuinely easy here — one empire is one file, and nothing else in the repo has to change.

**Highest-value work right now:**

1. **Build a missing empire** — `byzantine.html` and `russian.html` are already linked from the hub and currently lead nowhere.
2. **Add empires the tree doesn't cover yet** — Aztec, Inca, Qing, Carthage, Ethiopia/Aksum, Khmer, Songhai, Zulu, Austro-Hungary.
3. **Fill media gaps** — a phase with thin coverage that you know a film or documentary for.
4. **Fix accuracy** — wrong date, wrong watch order, a title that doesn't actually cover the phase it's filed under.

**To add an empire:**

1. Copy the closest existing empire file as your starting shell (`ottoman.html` is a good mid-size example; `rome.html` is the maximal one).
2. Read the *Phase Anatomy*, *Research Methodology* and *Exact HTML Boilerplate Templates* sections of [`PROJECT_BIBLE.html`](PROJECT_BIBLE.html) — they define the rules the collection is built on.
3. Change only the accent colour ramp. Keep the marble, the fonts, and the alternating layout.
4. Add the node to the hub tree in `index.html` on the correct lane — trunk, fork, or concurrent.
5. Every title you list must actually exist and must actually cover that phase. Cite nothing you haven't verified.

Open an issue first if you're taking on a whole empire, so two people don't build the same one.

## Roadmap

- [ ] Byzantine and Russian timelines (hub links already exist)
- [ ] Coverage beyond Eurasia — the Americas, Africa, Southeast Asia
- [ ] Where-to-watch availability hints per title
- [ ] A single continuous "world watch order" that interleaves all empires chronologically

## License

MIT — see [`LICENSE`](LICENSE).

---

<div align="center">

**If this is the watch order you've been looking for, star the repo** — it's how other people find it.

</div>
