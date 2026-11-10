# Spades Scorekeeper

A single-page, table-side scorekeeper for the Oh Hell–style Spades variant: register a game, enter players, track guesses and tricks, and keep running totals with bag penalties. Built to be passed around on an iPad in Safari.

**Play it here:** https://phanindrakannaji.github.io/spades-scorekeeper/

## Use it on an iPad

1. Open the link above in Safari (not Chrome).
2. Optional: Share → **Add to Home Screen** so it opens full-screen like an app.
3. Create a game, sit the iPad in the middle of the table, and pass it around for bids and scores.

Everything is saved on the device (Safari localStorage). No account, no network after the page has loaded. Use **Export** / **Import** if you want a JSON backup.

## Scoring (as implemented)

- Default **13 rounds**. Round *r* deals *r* cards per player. You can choose a different number of rounds when you start.
- The dealer rotates each round. The next player in seating order leads the first trick.
- Each player bids 0 through the number of cards in the round.
- **Made** (wins ≥ bid): **+10 × bid**, plus **+1** per extra trick (a bag). A made bid of 0 is 0 points, plus 1 per extra trick (no nil bonus).
- **Missed** (wins < bid): **−10 × bid**. No bags, no plus points.
- Bags accumulate. Every time a player reaches 5 bags they score **−50** and 5 bags are removed.

## Features

- Multiple saved games, resume, delete with confirm
- Big − / + steppers, no tiny inputs, landscape and portrait
- Bid and wins phases, with a running “tricks left” check
- Round summary, scoreboard, and final standings
- Edit any past round (totals and bags recalculate)
- Undo the last action
- Export / import JSON backups

The whole app is one self-contained `index.html` (inline CSS and JavaScript, no CDNs). You can also open that file directly in a browser.
