# Screenshots

Drop files in here using **exactly** these names and they appear on the home page
automatically. No HTML edit is needed.

| Filename | Caption already on the page | What to capture |
| --- | --- | --- |
| `01-start.png` | Choose a track and a mode | The library / start screen with a few tracks in it |
| `02-analyzing.png` | The beat map is built on your phone | The analyzing state |
| `03-trainer.png` | The 8-beat ring, counting live | A session mid-count, ring glowing |
| `04-reveal.png` | See exactly where your tap landed | The reveal map after a tap |
| `05-stats.png` | Progress across sessions | The stats screen with real numbers |

## Format

- **Portrait PNG.** 1290 × 2796 (iPhone 6.7") is ideal; anything close to 9:19.5 works — the
  frame uses `aspect-ratio: 9 / 19.5` and `object-fit: cover`, so a wildly different ratio will
  get cropped rather than letterboxed.
- **Export at 2×, not 3×.** The strip renders each shot about 260 px wide, so a 3× capture is
  wasted bytes.
- **Keep each file under ~500 KB.** These are loaded lazily, but five large PNGs still add up.
  `pngquant` or `oxipng` will usually halve a screenshot with no visible loss.
- **No device chrome.** The page draws its own phone frame around the image, so capture the
  screen content only — a screenshot with a bezel baked in will end up double-framed.
- Status bar is fine to leave in.

## While a file is missing

The frame renders as an empty device with a small label instead of a broken image, so it is safe
to add these one at a time. Adding fewer than five is fine too — but delete the unused `<figure>`
blocks from the screenshots section of `index.html` if you don't intend to fill them, otherwise
empty frames ship to production.

## Adding, renaming, or reordering

The slots live in `index.html` under the comment `SCREENSHOT SLOTS`. Each is one `<figure
class="shot">` block; copy one to add a sixth, or delete one to drop a slot.
