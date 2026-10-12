# AI Product Management: Hands-on Learning

A week-wise collection of small, browser-playable projects built as practical exercises in product thinking and implementation. Each game is a standalone HTML file with no external dependencies or build step.

## Week 01

### Memory Game

Play the [Memory Game](./Week-01/Memory-Game/memory-game.html), a Concentration-style matching game with 4×4 and 6×6 boards, a timer, move counter, star rating, saved best scores, and a persistent light/dark theme preference.

- [Memory Game PRD](./Week-01/Memory-Game/PRD_dark_theme.md)

### Snake

Play [Snake](./Week-01/Snake-Game/snake-game.html), a classic snake game with keyboard and touch controls, scoring, pause/resume, and a saved best score.

- [Snake PRD](./Week-01/Snake-Game/PRD_snake_game.md)

## Running the games

Open either linked HTML file directly in a modern browser. Alternatively, serve the repository root with a local HTTP server:

```bash
python3 -m http.server 8000
```

Then open the game links above, or visit:

- `http://localhost:8000/Week-01/Memory-Game/memory-game.html`
- `http://localhost:8000/Week-01/Snake-Game/snake-game.html`

Scores and preferences are kept in browser local storage.

## Project context

See [context.md](./context.md) for background on the original Memory Game.
