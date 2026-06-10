# The Protocol — 〈분리수거함〉 / Recycle Bin

A gesture for **Project 4: Protocol**, made for **ID.20012 (Design Studio 1)** at KAIST.

**Live site:** <https://leemyeongje.github.io/id20012-protocol/>

> The place doesn't change. The looking does.

---

## About the project

Every site has a protocol — the implicit rules that shape how people move through
it and what they do there, written not on signs but in the way people behave.
The brief asks you to read the protocol of one specific place on campus, then add
a single site-specific gesture that responds to it, and document the whole thing
on a webpage the class opens on their phones at the site.

## The gesture

I placed a **museum caption next to a recycling bin.**

People arrive at this corner with a single purpose: to throw something away. They
do it, and they leave. The site exists to be used without thought — and it is.
That thoughtlessness *is* its protocol.

The gesture doesn't change the place, only the frame around it. A museum caption
confers a kind of institutional attention: it quietly tells you that something
here is worth looking at, and how seriously to look. Placed beside a recycling
bin — an object everyone ignores — it transfers that same authority onto the act
of disposal, and for a moment the corner becomes something to stop and read. The
object stays exactly as it was; only the looking changes.

The caption card carries a QR code linking to a bilingual audio guide, completing
the borrowed museum apparatus.

> The full artist's statement — including the Duchamp reference and how the caption
> confers *place* rather than authorship — is on the [about page](about.html),
> with the source text in [`assets/texts/about.txt`](assets/texts/about.txt).

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
