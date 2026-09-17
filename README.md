# Friheten i Koden — CNDS Norway 2026 slides

Slidev deck for **"Friheten i Koden: Digital Sovereignty for the Nordic Age"**,
co-presented by Jeroen van Erp and Andrés Valero (SUSE) at Cloud Native Days
Norway, Bergen, 26–27 Oct 2026.

This replaces the earlier single-file `deck.html` prototype with a
markdown-driven deck ([Slidev](https://sli.dev)), so both presenters can edit
content as plain text/diffs instead of hand-editing HTML.

Content source of truth, talk brief, and full context (facts to keep
accurate, established conventions, the still-open speaker split) live in the
Obsidian vault, not here:
`~/Documents/avalero/SUSE/CNDS-Norway-2026/` — see `brief.md` there first.

## Usage

```bash
npm install
npm run dev      # http://localhost:3030 — live edit
npm run build    # static build, fully offline (venue has no internet)
npm run export   # PDF export
```

Keyboard: arrows/space to navigate, `f` for fullscreen, `o` for slide
overview, `d` toggles dark mode (deck is designed dark-first).

## Design system

Ported from Jeroen's original `deck.html` (see `HANDOFF.md` in the vault
folder): dark palette (`#0C121B` bg / `#131D2B` panel / `#E2A63D` gold accent
/ `#8FB0CF` steel), serif headlines, mono for data/terminal bits, thin-stroke
line icons, longship motif on the title and closing slide. Lives in
`style.css`, loaded automatically by Slidev.

## Status

19 slides, content ported from `outline.md` (vault). Speaker notes for
S7–S9 (Andrés's drafted block, split not yet confirmed with Jeroen) are
inline as HTML comments under each slide — visible in Slidev's presenter
mode (`npm run dev`, then the presenter view), not on the projected slide.
