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

## Layout

- `slides/` — the live Slidev source: `slides.md` (the deck) and `style.css`
  (design system, auto-loaded by Slidev since it sits next to the entry file).
  This is what you edit.
- `raw-content/` — `deck.html`, Jeroen's original single-file HTML draft.
  Kept as historical/reference raw content only; `slides/slides.md`
  explicitly superseded it as the editable source (see the note at the top
  of that file) and is not generated from it.

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

Ported from Jeroen's original `deck.html` (now in `raw-content/`; see
`HANDOFF.md` in the vault folder): dark palette (`#0C121B` bg / `#131D2B`
panel / `#E2A63D` gold accent / `#8FB0CF` steel), serif headlines, mono for
data/terminal bits, thin-stroke line icons, longship motif on the title and
closing slide. Lives in `slides/style.css`, loaded automatically by Slidev.

## Status

26 slides as of the 2026-09-17 storytelling pass (up from an initial
19-slide port of `outline.md`) — see the header comment at the top of
`slides/slides.md` for what changed and why; treat `outline.md` as
content/timing reference only, not a slide-number map for this file.
Speaker notes for S7–S9 (Andrés's drafted block, split not yet confirmed
with Jeroen) are inline as HTML comments under each slide — visible in
Slidev's presenter mode (`npm run dev`, then the presenter view), not on
the projected slide.
