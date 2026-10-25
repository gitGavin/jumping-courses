# Jumping Courses

A swimming-and-jumping game **designed by Noah, age 6, of Seattle**, and built with Claude and a little help from his dad.

## Play it

**Play now: https://gitgavin.github.io/jumping-courses/**

It works on a computer, phone or tablet. On a phone, turn it sideways so the GO and JUMP buttons sit on the left and right of the river.

**Play offline:** click `index.html` in this repo, click the **Download raw file** button (the down-arrow icon at the top right), then open the downloaded file in your browser. It is a single file with no install and no account. The title font loads from Google Fonts when you're online and falls back to a plain rounded font when you're not.

## How to play

- **GO** (hold): swim forward. On a keyboard: right arrow or `D`.
- **JUMP** (tap): leap. **Hold it longer to jump higher**, up to a limit. On a keyboard: `Space`, up arrow or `W`.
- Catch the leaping fish for **1 point each**.
- Jump over the obstacles. If one chomps you, a rescue boat carries you back, Mario-style. You have **5 hearts** per round. Lose them all and the round starts over.
- Pick any of **20 animal swimmers**, then pick which of the **10 rivers** to start from. Round 10 is the bonus round.
- Music and sound can each be turned off from the buttons under the river. A scoreboard ranks your runs.
- Secret: triple-tap the five hearts for unlimited lives in that round. Runs that use it are tagged "CHEATED" on the scoreboard.

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
10. **Emerald City**, a Seattle bonus round: Mount Rainier is the tallest peak, with the lower snowy Olympic and North Cascade mountains behind it, plus the Space Needle, a rainforest of evergreens, a lit-up Ferris wheel on the waterfront, bald eagles, seagulls and passenger jets in the sky, and rainy streets with glowing owl badges, a coffee-cup sign, a banana billboard and a smiling delivery-box sign. The obstacles are driftwood, ferries, salmon (they swim diagonally and turn red as they rise to the surface) and leaping orcas.

## The story

See [docs/how-it-was-built.md](docs/how-it-was-built.md) for how Noah's idea turned into a playable game.

## Tech

One self-contained HTML file: an HTML canvas game (800x500 logical canvas), plain JavaScript, no libraries or image files. Every character, creature and background is drawn in code. The music is generated live with the Web Audio API, with extra steps so sound works on phones (including iPhones on silent). Scores are stored in the browser's `localStorage` on each device only, so each device has its own scoreboard.
