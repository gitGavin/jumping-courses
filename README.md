# Jumping Courses

A swimming-and-jumping game **designed by Noah, age 6, of Seattle**, and built with Claude and a little help from his dad.

Open `index.html` in any browser to play. It is a single file with no install, no account and no internet needed (the title font loads from Google Fonts when online and falls back to a plain rounded font when offline).

## How to play

- **GO** (hold): swim forward. On a keyboard: right arrow or `D`.
- **JUMP** (tap): leap. **Hold it longer to jump higher**, up to a limit. On a keyboard: `Space`, up arrow or `W`.
- Catch the leaping fish for **1 point each**.
- Jump over crocodiles, sharks and stingrays. If one chomps you, a rescue boat carries you back, Mario-style. You have **5 hearts** per round. Lose them all and the round starts over.
- Pick any of **20 animal swimmers**, then pick which of the **10 rivers** to start from. Round 10 is the bonus round.
- Music and sound can each be turned off from the buttons under the river. A scoreboard ranks your runs.

## The 10 rivers

1. Sunny Meadow (easy swimming)
2. Jungle Creek (crocodiles arrive)
3. Sunset Canyon (stingrays and a shark)
4. Moonlit Marsh
5. Rainbow Rapids (the original final round, with a trophy)
6. Volcano Run (super hard)
7. Spooky Swamp (a current pulls you back)
8. Cosmic River (galaxy)
9. Digital Rain (Matrix-style)
10. Emerald City: a Seattle bonus round with Mount Rainier, the Space Needle, evergreens, a Ferris wheel, driftwood, ferries, salmon and leaping orcas

## The story

See [docs/how-it-was-built.md](docs/how-it-was-built.md) for how Noah's idea turned into a playable game.

## Tech

One self-contained HTML file: an HTML canvas game (800x500 logical canvas), plain JavaScript, no libraries or image files. Every character, creature and background is drawn in code. The music is generated live with the Web Audio API. Scores are stored in the browser's `localStorage` on each device only.
