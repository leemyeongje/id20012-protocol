# The Protocol — 분리수거함 / Recycle Bin

A small static site documenting a conceptual artwork: an ordinary recycling bin
reframed as a museum piece. Visitors scan a caption card placed beside the bin
and arrive at a bilingual (Korean / English) audio guide, then can read more
about the work itself.

> The place doesn't change. The looking does.

## Pages

- **`index.html`** — Audio guide. Korean / English language toggle, audio player,
  collapsible transcript, and a link to the about page.
- **`about.html`** — About this work. The work image followed by the artist's
  statement (The Protocol / What I Wanted / How the Experience Works), with a
  link back to the audio guide.

## Project structure

```
.
├── index.html              # audio guide
├── about.html              # about this work
└── assets/
    ├── audio/
    │   ├── korean.mp3       # Korean narration
    │   └── english.mp3      # English narration
    ├── images/
    │   └── trash.png        # work image
    ├── scripts/
    │   ├── script_korean.txt
    │   └── script_english.txt
    └── texts/
        └── about.txt        # source text for the about page
```

## Running locally

This is a plain static site — no build step. Because the pages load audio files,
serve it over HTTP rather than opening the files directly:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Editing content

- **Audio guide text** (title, transcript, audio paths) lives in the `content`
  object inside the `<script>` block of `index.html`.
- **About page text** is hard-coded in `about.html`; the source copy is kept in
  `assets/texts/about.txt`.
