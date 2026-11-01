# ⇧ Shift Runner

**[▶ Play Shift Runner](https://ashleywolf.github.io/shift-runner/)**

Six universes sit on top of one track. Run, dodge, and grab coins. When you hit a wall you can't get past, press **Shift**. You jump into a different universe at the exact same spot and keep running. Bounce between worlds to reach the finish line.

Made for [GitHub Game Off 2026](https://itch.io/jam/game-off-2026). Theme: **SHIFT**.

## How to play

| Key | Action |
| --- | --- |
| `←` `→` or `A` `D` | Change lanes |
| `↑`, `W`, or `Space` | Jump |
| `↓` or `S` | Slide (press in the air to drop fast) |
| `Shift` or `E` | Shift to the next universe |
| `P` or `Esc` | Pause |
| `M` | Mute |
| `R` | Restart |

On a phone or tablet, swipe to move, jump, and slide. Tap the **⇧ SHIFT** button to change universes.

### Tips

- **Read the icons at the top.** When a wall is coming, each universe shows ✅ (clear) or ⛔ (blocked).
- **Watch the corner box.** It shows the next universe on the track ahead, so you can see what you're shifting into.
- **Each universe has its own obstacles.** Shifting away from a wall can drop you in front of a log, a laser, or a cupcake. Plan your shift.
- **Space is floaty.** Jumps in Deep Space go higher and last longer.
- **On Windows,** pressing Shift five times in a row can open the Sticky Keys prompt. Use `E` instead, or turn off the Sticky Keys shortcut.

## The six universes

| | Universe | Look | Music |
| --- | --- | --- | --- |
| 🛕 | Jungle Temple | Stone paths, gold coins, a pyramid on the horizon | Tribal toms, marimba, and flute |
| 🌆 | Neon City | Synthwave grid, striped sun, glowing towers | Four-on-the-floor synthwave |
| 👾 | 8-Bit World | Four-color Game Boy green, chunky pixels | Pulse-wave chiptune |
| 🍭 | Candy Land | Pastel rainbow, lollipops, gumdrops | Music box and finger snaps |
| ✏️ | Notebook Doodle | Ink outlines on lined notebook paper | Lo-fi boom-bap with a kazoo lead |
| 🌌 | Deep Space | Stars, a ringed planet, floating asteroids, low gravity | Sub bass, slow pads, echoing bells |

All six worlds play the same song on the same beat. Shifting swaps the instruments without missing a note.

## How it works

- **One file, no build.** Everything lives in `index.html`. It loads [Three.js](https://threejs.org/) from a CDN. There are no asset files: the textures come from canvas drawings and the music from the Web Audio API.
- **One track, six outfits.** The level layout is shared. Each obstacle exists in some universes and not others. Shift walls block the whole track in some universes and are clear in the rest.
- **One clock.** A Web Audio step sequencer plays the song. Each step asks which universe you're in and plays that arrangement.
- **8-Bit World** renders at quarter resolution, then a shader snaps every pixel to the four Game Boy greens.

## Run it locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

To submit on itch.io, zip `index.html` and upload it as an HTML game.

## License

[MIT](LICENSE)
