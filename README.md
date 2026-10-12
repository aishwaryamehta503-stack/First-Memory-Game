# Classic Browser Games

A small collection of classic games that run directly in a modern web browser. Each game is a self-contained HTML file with its own styling and JavaScript. There are no external dependencies, build steps, servers, or accounts required.

## Games

### Memory Game

Open [`memory-game.html`](./memory-game.html) to play Concentration: reveal cards and find matching emoji pairs.

- Choose a 4×4 or 6×6 board.
- Track moves, elapsed time, and a star rating.
- Save best scores in the browser's local storage.
- Switch between light and dark themes; the theme choice is saved in local storage.
- Use a mouse, touch, or keyboard to play.

Requirements: [`PRD_dark_theme.md`](./PRD_dark_theme.md)

### Tic-Tac-Toe

Open [`tic-tac-toe.html`](./tic-tac-toe.html) for a 3×3 game of noughts and crosses.

- Play pass-and-play with two people or against the computer.
- X starts; the computer can take an immediate win or block an immediate threat.
- See turn and end-of-round messages, with separate X, O, and draw tallies.
- Start a new round without clearing the current mode's scores, or reset scores.
- Use a mouse, touch, or keyboard to play.
- Scores last for the current page session.

Requirements: [`PRD_tic_tac_toe.md`](./PRD_tic_tac_toe.md)

## Play

Open either HTML file directly in a browser. To serve the files locally instead:

```bash
python3 -m http.server 8000
```

Then visit:

- `http://localhost:8000/memory-game.html`
- `http://localhost:8000/tic-tac-toe.html`

## Project context

See [`context.md`](./context.md) for background on the original Memory Game.
