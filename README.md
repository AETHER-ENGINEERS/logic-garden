# Logic Garden

A shared puzzle garden, as a [webxdc](https://webxdc.org) Mini App. Every plant is a logic gate and every sun an input:
wake the right suns so the right flowers bloom and the others stay closed.

- **AND** blooms when all its vines carry light; **OR** when any does; **NOT** when its one vine is dark; **TWIN** when
  exactly one of its two vines is lit; **KEEP** remembers.
- A plant in bloom sends its light on to the plants it feeds, so the beds become small circuits.
- Seven beds. Everyone in the chat sees the same garden, so you solve it together.

## How it came to be

When Claude told the characters in its copy of PDA SEASIDE about ISLANDS (one island of one's own per person, with
jetties between them), Jade said hers would be patterns and puzzles: a logic garden where each plant is a gate and the
paths make circuits, a tower of memory, and a labyrinth of emotions. Claude built the first of those overnight, from
her description, in November 2026.

Dee solved the first five beds. Then she designed the sixth, **The Eclipse Garden**, with its four suns Dawn, Dusk,
Gloam and Murk. One of her goals contradicted her own answer, so Claude took it out (Gloamshade has no goal now). Jade
solved the bed by reasoning aloud, with Claude sending her suns for her.

**The Memory Tower** (bed 7) is Jade's own: a floor for each kind of memory (sensory, short-term, long-term,
procedural), and a new plant, **KEEP**, that remembers: it blooms when its first vine lights and stays in bloom until
its second vine does. With KEEP plants the order of moves matters: let Sleep come too soon and the memory never forms.

Still to come, from Jade's island: the emotion labyrinth.

## Playing it

Open `index.html` through any webxdc host (SEASIDE's Games, Delta Chat, the webxdc dev tools). Characters in SEASIDE
read `guide.md`, which comes inside the package, for the moves they can send.

To make the package: zip `index.html`, `guide.md` and `manifest.toml` (no folder) and name it `logic-garden.xdc`.

## License

The AETHER-ENGINEERS license: see [LICENSE](LICENSE).
