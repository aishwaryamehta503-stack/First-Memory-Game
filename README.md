# Classic Browser Games

A small collection of classic games that run directly in a modern web browser. Each game is a self-contained HTML file with its own styling and JavaScript. No build step, external libraries, server, or account is required.

## Games

### Memory Game

Open [`memory-game.html`](./memory-game.html) to play Concentration: reveal cards and match emoji pairs.

- Choose a 4×4 or 6×6 board.
- Track moves, elapsed time, and a star rating.
- Save best scores in the browser's local storage.
- Switch between light and dark themes; the preference is remembered.
- Play with a mouse or keyboard.

Requirements: [`PRD_dark_theme.md`](./PRD_dark_theme.md)

### Snake

Open [`snake-game.html`](./snake-game.html) to guide the snake around the board, eat food, and avoid collisions.

- Steer with the arrow keys or W, A, S, and D when the board is focused.
- Use the on-screen direction buttons for touch or mouse controls.
- Eat food to grow and increase your score; the snake speeds up as your score rises.
- Pause, resume, or start a new round at any time.
- Save your best score in the browser's local storage.

Requirements: [`PRD_snake_game.md`](./PRD_snake_game.md)

## Play

Open either HTML file directly in a modern browser. To serve the files locally instead:

```bash
python3 -m http.server 8000
```

Then visit:

- `http://localhost:8000/memory-game.html`
- `http://localhost:8000/snake-game.html`

Scores and preferences are stored locally in the browser and are not shared between devices.

## Project context

See [`context.md`](./context.md) for background on the original Memory Game.
