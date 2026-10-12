# Repository Context

## What this project is

This repository contains a browser-based Memory Game, also known as Concentration. The name describes the game; it does not stand for a separate acronym.

## What it does

Players reveal cards and find matching emoji pairs. The game offers two board sizes:

- **4×4:** 8 pairs
- **6×6:** 18 pairs

It counts moves, tracks elapsed time, and awards a three-star rating based on the number of moves. When all pairs are matched, it shows the final stats and saves up to five best scores in the browser's local storage.

## How it is built

The game is implemented in `memory-game.html` as a single standalone file containing the page markup, responsive CSS, and JavaScript game logic. It has no external libraries, build step, or backend. Cards are shuffled with the Fisher–Yates algorithm. The interface supports mouse and keyboard play, uses ARIA roles and state attributes, and adapts to smaller screens.

## How to run

Open `memory-game.html` in a modern web browser. Alternatively, serve the repository with a local HTTP server and open `/memory-game.html`. Scores are stored in that browser's local storage and are not shared between browsers or devices.

## Repository contents

- `memory-game.html` — the complete game
- `README.md` — quick-start instructions and feature overview
- `context.md` — this project context
