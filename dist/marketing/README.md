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
| `house-hero.jpg` | Hero, right half of the band, bleeding off the edge | 4:3 | One house. The record card overlaps its left, so keep the subject right of centre |
| `record-boiler.jpg` | Record band, on the "Boiler fitted" entry | 4:3 | The boiler on the wall |
| `record-repair.jpg` | Record band, on "Annual service" | 4:3 | A plumber working on pipework |
| `record-document.jpg` | Record band, on "Annual service and gas safety check" | 4:3 | The receipt and the certificate |
| `record-room.jpg` | Record band, on "Autumn walk-round" | 4:3 | A room, as somebody walking round would see it |
| `check-wide.jpg` | Checks band, above the three cards | 16:9 | Somebody with no stake, at the property, photographing it |

**Each record photograph is attached to the entry it illustrates**, beside it
on a desktop and under its text on a phone. That is the only arrangement that
works here. Gathering them into a strip below the logbook was tried and it
read as decoration bolted onto a record, because none of the four was the
thing any particular entry named. Two entries carry no photograph on purpose:
not every line of a real record has one.

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
- **Keep them small.** Export at about 1600px on the long edge, JPEG quality
  ~75, or WebP. These ship inside the demo bundle, which is served from
  GitHub Pages.
- **No recognisable address or number plate**, since the product is about
  real property and a real door number in an advert is somebody's house.
