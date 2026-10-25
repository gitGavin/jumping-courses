# How Jumping Courses was built

## The short version

Noah, a 6-year-old boy who lives in Seattle, had an idea for a game. He described it out loud, his dad's voice-to-text turned his words into text, and Claude (Anthropic's AI assistant) wrote the game. Noah's dad guided the conversation, tried each version with Noah, and passed on the next round of ideas. The whole game is one HTML file.

Noah designed the game. Claude wrote the code. Dad was the go-between and tester.

## How the work happened

1. **Noah talks, voice-to-text writes.** Noah explained the game he wanted in his own words. The conversation was captured with voice-to-text, so the first message reads like a kid talking, not like a software spec. Claude read it and turned it into a plan.
2. **Claude builds, the family plays.** Claude wrote a working version. Noah and his dad played it, said what felt too hard, too easy, or missing, and sent that back as the next request.
3. **Repeat.** Each idea became a small change, a new build and a quick test, then another round of play. The game grew over many of these rounds.
4. **Check before sharing.** For each change Claude ran the game's code in an automated test and looked at screenshots of the new parts. Early on, a scoreboard bug showed up in play, so the scoreboard was rebuilt using only real scores from real runs.

## What Noah asked for first

From the original conversation:

- The game is called **Jumping Courses**.
- There is no single main character. Players choose from **about 20 characters**.
- There are **5 rounds**, each harder than the last.
- Every round is a **river with a different environment**.
- Round 1 is easy swimming. Round 2 adds **crocodiles**. **Fish** can be collected, worth **1 point** each.
- If you get chomped, you are **rescued, like in Mario**. If you die, you **start the round over**.
- In rounds 3 to 5 the fish get faster, and **stingrays** are another danger.

## How the game grew

Each step below started as something Noah or his dad asked for.

- Make the fish easier to catch.
- Add a **shark**.
- Show a **trophy** after finishing round 5.
- Go from 3 lives to **5 lives**, and make rounds 1 to 4 easier while keeping round 5's difficulty.
- Add a **super-hard round 6**.
- Make the **jump button hold-to-jump-higher**, with a limit on the height.
- Add **background music** and a **scoreboard** ranked from highest to lowest with your own run highlighted.
- Try a back button, decide it wasn't helping, and remove it.
- Add a **round-select screen**, starting on round 1.
- Add rounds 7 to 10 with imaginary themes (**Halloween, galaxy, Matrix-style** and more), with round 10 as the bonus.
- Fix a scoreboard bug found while playing (a finished 41-point run was missing) by rebuilding it from real data.
- Turn round 10 into a **Seattle** round: Mount Rainier with glaciers, the Space Needle, a rainforest of evergreens and a rainy Pacific Northwest sky.
- Add a secret **triple-tap-the-hearts cheat** for unlimited lives in a round. Runs that use it are tagged "CHEATED" on the scoreboard.
- Move the GO and JUMP buttons to the sides of the screen and make the river bigger when the phone or tablet is held sideways.
- Fill out Seattle: a Ferris wheel on the waterfront, a banana billboard, a green-and-white owl badge, rain with falling coffee cups and bananas that give bonus points, and obstacles of driftwood, ferries, salmon (they turn red as they rise to the surface) and leaping orcas.

- Make the Seattle round look bigger: Mount Rainier is the tallest peak, with the Olympic and North Cascade mountains behind it.
- Make coffee and bananas count as fish, so the bonus points show up in the fish counter.
- Fix missing sound on phones (iPhone silent switch and paused audio), and publish the game through GitHub so anyone can play from a link.

## Choices made along the way

- **One file, no libraries.** Everything is drawn with code, so the game runs anywhere and is easy to share.
- **Kid-sized difficulty.** Early rounds are gentle, and the hardest ones are optional. Noah can start on any round.
- **Real data only.** After the scoreboard bug, the scoreboard shows only runs that were actually played.
- **Original art.** The characters, creatures and signs are original drawings. Real company logos were left out on purpose, and original badges and signs were used instead.

## Files in this repo

- `index.html`: the whole game.
- `README.md`: how to play.
- `docs/how-it-was-built.md`: this story.
