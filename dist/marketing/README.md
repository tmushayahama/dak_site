# Marketing photographs

Drop files here by the exact names below and they appear on the site. Until a
file exists its slot renders nothing, so the page is never broken by a missing
one and every photograph added is strictly an improvement.

Referenced through `src/features/marketing/Photo.tsx`, which resolves them
against `import.meta.env.BASE_URL`. Do not hard-code `/marketing/...`
anywhere: the demo ships under `/dak_site/` and a root-relative path 404s
there while working in development.

| File | Where | Ratio | What it is |
| --- | --- | --- | --- |
| `house-hero.jpg` | Hero, behind the whole band, under the page's cream on the left | 16:9 | One house. Keep the subject right of centre, where the cream thins |
| `t-look.jpg`, `t-repair.jpg`, `t-document.jpg`, `t-room.jpg` | The hero's phone, as the thumbnails on its record | 4:3, the look 16:9 | Small: the look, a repair, the paper, a room |
| `m-room.jpg`, `m-boiler.jpg`, `m-document.jpg`, `m-look.jpg` | Record band, heading the card of the entry each illustrates, its title on the picture's foot | 4:3, the look 16:9 | A room walked at move-in, the boiler, the inspector's signed report, the independent look |
| `strip-owner.jpg` | A strip after Who it is for, one line on its quiet right | 21:9 | Somebody in their own sunlit living room photographing a chip in the skirting, left of centre; the right a plain wall for the words |
| `strip-traveller.jpg` | A strip above the footer, one line on it, mirrored from `md` | 21:9 | A guest photographing a hotel room's minibar on the first evening, right of centre |
| `strip-caretaker.jpg` | Behind One book, under the cream on the right where its words are, and after them on a phone | 21:9 | Somebody walking round a yard, checking the tank, right of centre |
| `check-wide.jpg` | Top of the Checks page, across it under the page's head | 16:9 | Somebody with no stake, at the property, photographing it |
| `independence-wide.jpg` | Behind the dark band, under its own colour | 21:9 | A kitchen table at night: keys, a receipt, a phone showing a crack. The left half nearly black, where the words are |
| `final-wide.jpg` | Behind the last band, under the cream on the left | 21:9 | Somebody at the open gate of a house, phone in hand, right of centre |

A photograph behind a band (`house-hero`, `independence-wide`, `final-wide`)
keeps its subject right of centre and its left side quiet, because the words
sit there. A strip carries one line on its quiet side and is cropped toward its
subject on a phone, so keep the subject a little in from the edge.

**Each record photograph heads the card of the entry it illustrates**, the
entry's title set on its foot over a dark blend. The stamp, the year and who
said it stay on the card's own ground, never on the picture (the one rule
below). Gathering the photographs into a strip below the logbook was tried and
it read as decoration bolted onto a record, because none of the four was the
thing any particular entry named. On the hero's phone most entries carry no
photograph, on purpose: not every line of a real record has one.

## The one rule

**A photograph here never goes inside a record card, a report, or beside an
evidence stamp.** `src/data/frames.ts` explains it for seeded captures and it
applies to marketing for the same reason: a real capture carries a location
fix and a server timestamp, and scenery standing where a reader expects
evidence invites them to judge evidence that is not evidence. Photographs go
behind, beside and above the product. Never in it.

## Practical notes

- **Where to get them.** Unsplash and Pexels both allow commercial use with no
  attribution. Search the object rather than the mood: "boiler cupboard",
  "electricity meter", "damp ceiling", "terraced house door", "handing over
  keys". Searching "luxury home" gets the wrong thing every time.
- **People, if any, are in a role.** A contractor at a repair, somebody at a
  doorway, somebody photographing a wall. No handshakes, no suits, no
  headsets, nobody smiling at a laptop.
- **Keep them small.** From the repo root,
  `uv run scripts/images/compress.py <picture> -o <this folder>/<name>.jpg`
  makes a JPEG under 300 KB at the best quality that fits, with no metadata
  (`scripts/images/README.md`). These ship inside the demo bundle, which is
  served from GitHub Pages.
- **No recognisable address or number plate**, since the product is about
  real property and a real door number in an advert is somebody's house.
