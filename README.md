# The Protocol — 〈분리수거함〉 / Recycle Bin

A gesture for **Project 4: Protocol**, made for **ID.20012 (Design Studio 1)** at KAIST.

The work places a museum-style caption card beside an ordinary recycling bin and
hands the viewer a bilingual (Korean / English) audio guide — borrowing the
institutional authority of a museum to make people stop and look at a place they
normally pass without a thought.

**Live site:** <https://leemyeongje.github.io/id20012-protocol/>

> The place doesn't change. The looking does.

---

## The brief

> **Project 4: Protocol**
>
> Every site has a protocol: a set of implicit rules about how people move
> through it, how long they stay, and what they do there. Most protocols are not
> posted on signs. They are written in the way people behave. The shortcut made
> across the grass because the path is far away. The staircase nobody uses
> because the elevator is right there. The window at the end of the hallway that
> no one stops to look out of.
>
> This project asks you to **read the protocol of a specific site**, then **add a
> gesture that responds to what you found**.
>
> 1. **Site** — somewhere you can walk to on campus (N25 preferred), visit more
>    than once, and bring the class to on presentation day. It must be specific.
> 2. **Gesture** — one site-specific act of addition: an object, a mark, a text,
>    a light, a sound, or an arrangement. Temporary or permanent. Nothing illegal;
>    if it requires permission, get permission first.
> 3. **Document** it — photograph it, write about what you found, what you did,
>    and what happened — and present everything through a webpage viewable on
>    mobile.
> 4. On presentation day, the class walks to your site and opens your URL on
>    their phones.

The gesture must answer four questions:

- What is the protocol of this site?
- What did you want to change, reveal, or make visible?
- Why this addition, and not something else?
- What impact did it bring?

---

## The gesture

I added a **museum caption next to a recycling bin.**

### What is the protocol of this site?

People arrive at this corner with a single purpose: to throw something away. They
do it, and they leave. The site exists to be used without thought — and it is.

### What did you want to reveal?

To make someone stop. Not by changing the place, but by changing the frame around
it. A museum caption confers a kind of institutional attention onto an object
everyone ignores; for a moment, the disposal site becomes something to look at.
The place doesn't change — the looking does.

### Why this addition, and not something else?

A museum caption quietly signals to a viewer that there is something specific here
worth looking at. It does this without altering the object at all — exactly the
minimal, frame-only intervention the work needs.

> The full artist's statement (including the Duchamp reference and how the
> caption confers *place* rather than authorship) is on the
> [about page](about.html), with the source text in
> [`assets/texts/about.txt`](assets/texts/about.txt).

---

## The webpage

A plain static site — no build step — designed mobile-first for presentation day.

### Pages

- **`index.html`** — the audio guide reached by the QR code on the caption card.
  Korean / English language toggle, audio player, and a collapsible transcript.
- **`about.html`** — documentation of the work: the installation photos and the
  artist's statement.

The two pages link to each other.

### Structure

```
.
├── index.html              # audio guide
├── about.html              # about this work
└── assets/
    ├── audio/              # korean.mp3, english.mp3 — narration
    ├── images/            # installation photos + work image
    ├── scripts/           # audio-guide transcripts (ko / en)
    └── texts/             # source text for the about page
```

### Deployment

Hosted on **GitHub Pages** from the `main` branch — every push to `main` is
published automatically at the live URL above.
