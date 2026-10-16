# Perry_Trapdoors

Animated, synced **secret doors and trapdoors** for **RedM** servers running the VORP framework – hidden bookshelf passages, gunsmith floor hatches, smuggler cellars and more.

## Features

- **Wall doors** (e.g. a bookshelf that swings open) and **floor trapdoors** (hatches that lift up).
- Smooth opening and closing animation.
- **Synced to all players** – when one player opens a door, everyone sees it open.
- Hold-to-open prompt using VORP utils.
- Add as many doors as you want from `config.lua`.

## Installation

1. Download or clone this repository into your server's `resources` folder.
2. Add it to `server.cfg` after its dependencies:
   ```cfg
   ensure vorp_utils
   ensure Perry_Trapdoors
   ```
3. Restart the server.

## Configuration

Add doors to `Config.TrapDoors` in `config.lua`:

```lua
{
    x = 2858.92, y = -1194.85, z = 47.98,   -- door position
    name = "kirjastohylly",                 -- unique name
    doorProp = `s_clothingcasedoor01x`,     -- door model
    closedRotX = 0.0, closedRotY = 0.0, closedRotZ = 93.47,   -- rotation when closed
    openRotX = 0.0,   openRotY = 0.0,   openRotZ = 154.46,    -- rotation when open
    walldoor = true,  floordoor = false,    -- type of door
},
```

- **Wall doors** rotate around the Z axis (`closedRotZ` → `openRotZ`).
- **Floor doors** rotate around the X axis (`closedRotX` → `openRotX`, typically `0.0` → `-90.0`).

The config ships with three examples: a bookshelf passage in Saint Denis, a gunsmith trapdoor in Rhodes and one more floor trapdoor.

## Requirements

- RedM server (`rdr3`)
- [VORP Core](https://github.com/VORPCORE/vorp-core-lua) with **vorp_utils**

## Support

Found a bug or have an idea? [Open an issue](https://github.com/JuhaP2/Perry_Trapdoors/issues).
If this script is useful for your server, a ⭐ on the repo is appreciated!
