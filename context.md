# Repository Context

## What this project is

This repository contains a browser-based Memory Game, also known as Concentration. The name describes the game; it does not stand for a separate acronym.

## What it does

Players reveal cards and find matching emoji pairs. The game offers two board sizes:

- **4×4:** 8 pairs
- **6×6:** 18 pairs

It counts moves, tracks elapsed time, and awards a three-star rating based on the number of moves. When all pairs are matched, it shows the final stats and saves up to five best scores in the browser's local storage.

## How it is built

The game is implemented in `Week-01/Memory-Game/memory-game.html` as a single standalone file containing the page markup, responsive CSS, and JavaScript game logic. Its dark-theme requirements are documented in `Week-01/Memory-Game/PRD_dark_theme.md`. It has no external libraries, build step, or backend. Cards are shuffled with the Fisher–Yates algorithm. The interface supports mouse and keyboard play, uses ARIA roles and state attributes, and adapts to smaller screens.

## How to run

Open `Week-01/Memory-Game/memory-game.html` in a modern web browser. Alternatively, serve the repository with a local HTTP server and open `/Week-01/Memory-Game/memory-game.html`. Scores are stored in that browser's local storage and are not shared between browsers or devices.

## Repository contents

- `Week-01/Memory-Game/memory-game.html` — the complete Memory Game
- `Week-01/Memory-Game/PRD_dark_theme.md` — dark-theme requirements
- `Week-01/Snake-Game/snake-game.html` — the complete Snake game
- `Week-01/Snake-Game/PRD_snake_game.md` — Snake requirements
- `README.md` — project overview and game links
- `context.md` — this project context
