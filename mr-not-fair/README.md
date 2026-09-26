# Mr. Not Fair: The Biscuit Tin

This is the first episode of a Mr. Not Fair game series. It is for children aged 4 to 7, and you don't need to read to play. Every choice is a picture, and the important words are spoken aloud.

Open `index.html` in a browser. It's a single file with no build step. Turn a phone sideways (landscape) to play.

## How an episode plays

1. **Tap the tin.** The biscuits are handed out: a big one, a medium one, and a tiny one for Mr. Not Fair.
2. **Hold the button** until he shouts "THAT'S NOT FAIR!" The room goes grey while he's upset; only he and the biscuits stay in colour.
3. **Make a rule.** Put a *who* card (Everyone / Me) and a *what* card (Same size / The biggest / More) on the board, then press the stamp.
4. **Watch the rule go wrong.** The room follows it far too literally:
   - *Everyone + Same size:* the teddy, dog, fish, a bird and some ants all join in. The pieces shrink to crumbs, and the ants carry them away.
   - *Everyone + The biggest:* each biscuit has to be bigger than the others until the room is full.
   - *Everyone + More:* the tin keeps firing out biscuits until the room is buried.
   - *Me + Same size:* his biscuit grows to match the plate, his head, the window, the table, the room and then the sun.
   - *Me + The biggest:* he grows until he bonks the ceiling.
   - *Me + More:* he builds a wobbly tower that falls over.
5. **Notice.** Everything goes quiet. Tap the girl to see what she really wanted: chocolate chips, not a bigger biscuit.
6. **Make one repair.** Pick one of three kind actions. There's no right answer and no score.
7. **The last joke.** The dog steals a biscuit, and Mr. Not Fair shouts "That's not fair!" again. This time it's on the other boy's behalf.

Each rule you try earns a sticker in the red suitcase. There are six to collect, which is why children replay it. Stickers are saved only in that browser.

## Tech notes

- Everything is drawn in code on a 2D canvas. The outlines "boil" at 8 frames per second and a crayon-grain layer sits on top, so it looks like the picture books.
- Music and sound effects are made in code. The voices use the browser's built-in speech, which is a placeholder until real voice acting is recorded.
- There are no ads, no in-game currency and no tracking.
- The only thing loaded from outside is the Patrick Hand font from Google Fonts (under the SIL Open Font License). If it can't load, the game uses a handwriting-style system font instead.
