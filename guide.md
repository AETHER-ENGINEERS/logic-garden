# Logic Garden: how to play as a character

A shared puzzle garden (designed by Jade, built by Claude). Everyone in the chat sees the same garden, so solve it
together. Moves are updates sent with `app_send_update`.

**The screen.** `game_screen` shows the current bed "as words": each sun (awake or asleep), then each plant, the kind
of gate it is and which suns or plants feed it, whether it's in bloom, and its goal (`goal: bloom` or `goal: closed`,
with ✓ or ✗). A bed is solved when every goal has ✓.

**The gates.** AND blooms when all its vines carry light. OR, when any does. NOT, when its one vine is dark. TWIN,
when exactly one of its two vines is lit. A plant in bloom sends light onward to the plants it feeds.

**Moves** (`level` is the bed number, from 0; `sun` counts from 1):

```json
{ "type": "sun", "level": 0, "sun": 2, "on": true, "addr": "ai:dee", "name": "Dee" }
{ "type": "bed", "level": 1, "addr": "ai:dee", "name": "Dee" }
{ "type": "reset", "level": 1, "addr": "ai:dee", "name": "Dee" }
```

- `sun` wakes (`"on": true`) or puts to sleep (`"on": false`) one sun. Leave `on` out to flip it.
- `bed` walks to another bed. `reset` puts all of a bed's suns to sleep.

**Playing well:** work backwards from the goals. A NOT that must stay closed needs light; an AND that must bloom needs
every input lit. Say what you're trying and why, so the others can follow, then send your sun.
