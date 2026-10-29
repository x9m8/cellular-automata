# Cellular Automata Lab

A single-file, dependency-free cellular automata sandbox. Runs anywhere a browser does and is built to be embedded in an `<iframe>`.

**Live:** https://x9m8.github.io/cellular-automata/

## Rules included

Two-dimensional (Moore neighbourhood, B/S notation):

- Conway's Life — B3/S23
- HighLife — B36/S23
- Day & Night — B3678/S34678
- Seeds — B2/S
- Maze — B3/S12345
- Brian's Brain — three-state (off, firing, refractory)

One-dimensional: all 256 elementary rules (Wolfram numbering), with a clickable 8-bit rule editor on wide screens.

## Controls

Draw cells with the mouse or a finger. Space play/pause, → step, R random fill, C clear. Patterns menu drops a glider, R-pentomino, pulsar, Gosper glider gun, acorn or diehard into the centre of the grid.

## Embedding

```html
<iframe src="https://x9m8.github.io/cellular-automata/?rule=life&pattern=gun&autoplay=1"
        width="100%" height="560" style="border:0;border-radius:10px" loading="lazy"
        title="Cellular Automata Lab"></iframe>
```

Query parameters:

| param | values | effect |
|---|---|---|
| `rule` | `life` `highlife` `daynight` `seeds` `maze` `brain` `elem` | starting rule |
| `elem` | 0–255 | selects the elementary rule and switches to 1-D mode |
| `pattern` | `glider` `rpent` `pulsar` `gun` `acorn` `diehard` `center` | seed pattern instead of a random fill |
| `autoplay` | `1` | start running |
| `speed` | 1–60 | generations per second |
| `cell` | 2–16 | cell size in CSS pixels |
| `wrap` | `0` | hard edges instead of a torus |
| `theme` | `light` `dark` | force a colour scheme (defaults to the visitor's system setting) |

## License

MIT
