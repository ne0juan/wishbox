# Wishbox visual test prototype

Open `index.html` in a browser. This is a local, static interaction prototype. It has no backend and does not persist the text entered by a participant.

## Design direction

The provided Kifune Shrine screenshot is a **mood reference**: open space, pale forest green, water blue, thin ink-like linework, and restrained typography. The prototype uses original CSS/SVG scenery; it does not reproduce the shrine's map or religious symbols.

| Role | Color |
| --- | --- |
| Paper background | `#f7f9f6` |
| Pale forest | `#dcebe3` |
| Water | `#c7e4e9` |
| Text | `#334b57` |
| Line | `#b8d0cc` |
| Small seal accent | `#b77f73` |

## Experience

1. Choose a topic. Both reveal options have equal size and visual treatment.
2. Open **a reading**: touch the paper over water; the authored text develops over 1.5 seconds.
3. Write a short wish on a paper slip. Sharing is opt-in and unchecked by default.
4. Fold and post the slip into a Wishbox mailbox. The mailbox is a contemporary product metaphor inspired by the physical act of submitting a prayer letter at Meiji Jingu, not a digital shrine.
5. Open a stranger's wish and optionally write a reply. The demo text is prominently labeled as an example. A real study must use consenting, reviewed submissions and replies.

## Test integrity

The original seven-day question is whether users choose another personal reading or an unknown real wish after trying both. Keep both entrances equally prominent and randomize their order in the actual study. Record the first choice before any post-reading invitation to write a wish. This static prototype only shows the interaction and does not log events, randomize position, submit content, moderate, or send replies.

The reading and mailbox animations respect `prefers-reduced-motion`. Before a live study, build an explicit delete flow and a reviewed-content pipeline as described in the root README.
