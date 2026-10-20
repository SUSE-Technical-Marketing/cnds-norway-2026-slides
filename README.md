# Friheten i Koden · CNDS Norway 2026 slides

Slidev deck for **"Friheten i Koden: Digital Sovereignty for the Nordic Age"**,
co-presented by Jeroen van Erp and Andrés Valero (SUSE) at Cloud Native Days
Norway, Bergen, 26–27 Oct 2026.

This replaces the earlier single-file `deck.html` prototype with a
markdown-driven deck ([Slidev](https://sli.dev)), so both presenters can edit
content as plain text/diffs instead of hand-editing HTML.

Content source of truth, talk brief, and full context (facts to keep
accurate, established conventions, the still-open speaker split) live in the
Obsidian vault, not here:
`~/Documents/avalero/SUSE/CNDS-Norway-2026/`. See `brief.md` there first.

## Layout

- `slides/` is the main deck: `slides.md` (26 slides), `style.css` (the Viking
  voyage theme) and `global-top.vue` (the voyage bar: a longship that sails
  along the bottom, with one waypoint per chapter). This is what you edit.
- `slides/components/` holds the Viking illustrations, usable in any slide:
  `<Viking variant="real|myth" />`, `<Axe />`, `<Shield a="#color" b="#color" label="JE" />`
  and `<Longship />`. All hand-drawn SVG, so the deck stays fully offline.
- `raw-content/deck.html` is Jeroen's single-file HTML deck of 22 Sep 2026,
  kept for reference.
- `archive/2026-09-17-andres-slidev/` is Andrés's earlier Slidev pass of
  17 Sep 2026, kept for reference. Run it with
  `bunx slidev archive/2026-09-17-andres-slidev/slides.md`.

The main deck merges both versions (6 Oct 2026) into one story line: the talk
is a voyage in seven chapters (the myth, the keel, foreign waters, the charts,
shipbuilding, sea trial, home port). The header comment in `slides.md` maps
chapters to slides and speakers.

## Usage

```bash
bun install
bun run dev      # http://localhost:3030  live edit
bun run build    # static build, fully offline (venue has no internet)
bun run export   # PDF export
```

Keyboard: arrows/space to navigate, `f` for fullscreen, `o` for slide
overview, `d` toggles dark mode (deck is designed dark-first).

### Shield centers

The shield supports three center styles, in priority order:

- Photo: `<Shield photo="/jeroen.jpg" />` crops the image to a circle inside
  the shield. Put local photos in `slides/public/` to keep the deck offline.
- Initials: `<Shield label="JE" />` uses the existing gold-on-dark badge.
- Knob (shield boss): `<Shield />` shows the metal center when neither is set.

If both `photo` and `label` are provided, the photo takes precedence. The
`size`, `a`, and `b` props work with all three styles.

## Design system

Ported from Jeroen's original `deck.html` (now in `raw-content/`; see
`HANDOFF.md` in the vault folder): dark palette (`#0C121B` bg / `#131D2B`
panel / `#E2A63D` gold accent / `#8FB0CF` steel), serif headlines, mono for
data/terminal bits, thin-stroke line icons, longship motif on the title and
closing slide. Lives in `slides/style.css`, loaded automatically by Slidev.

## Status

26 slides, merged 2026-10-06. Still open: confirm the speaker split with
Jeroen (the deck assumes Andrés takes chapter IV, the charts) and do a timed
run-through, since content is about 25 minutes in a 30-minute slot. Speaker
notes are HTML comments under each slide, shown in presenter mode.
