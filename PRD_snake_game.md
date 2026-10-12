# Product Requirements Document: Snake

## Overview

Create a classic Snake game as a standalone HTML file that can be opened and played in a modern browser. The player steers a snake around a board, eats food to grow and score, and tries to avoid colliding with the walls or its own body.

## Goals

- Deliver an immediately understandable, playable version of classic Snake.
- Keep all markup, styling, and game logic in one HTML file with no external dependencies.
- Support keyboard play on desktop and touch-friendly directional controls on small screens.
- Make starting, pausing, resuming, and starting a new round explicit and reliable.
- Track the current score and best score without changing or depending on other games' data.

## Out of scope

- Multiplayer, online leaderboards, accounts, or server-side score storage.
- Custom board sizes, themes, skins, or difficulty settings.
- Sound effects or external assets.

## Gameplay

- The board is a fixed 20-by-20 grid.
- A new round begins with a short snake moving across the board and one food item placed in an unoccupied cell.
- Each food item eaten grows the snake by one segment and increases the score by one.
- The snake moves continuously and wraps neither through walls nor through itself. A collision ends the round.
- The movement speed increases gradually as the score rises, with a reasonable upper limit.
- Food placement must never overlap the snake. If the board is filled, end the round as a win rather than placing invalid food.

## Controls and states

- Provide visible **Start / Play again**, **Pause / Resume**, and four directional controls.
- Arrow keys and WASD steer the snake when the board is focused; directional buttons provide touch and mouse input.
- Prevent immediate 180-degree reversals and prevent a second turn from being queued before the next movement step.
- Ignore game controls while the round is not running, except starting or resuming through their buttons.
- Show a clear ready, paused, or game-over message and provide a straightforward way to begin a fresh round.

## Score and persistence

- Show the current score and best score.
- Persist the best score in local storage under a Snake-specific key. Do not use or modify keys belonging to other games.
- If storage is unavailable, allow the game to run with the current score and a session-only best score.

## Accessibility and responsive behavior

- Use semantic buttons with clear accessible names and visible keyboard focus.
- Make the board perceivable to assistive technology with a concise accessible label and expose state/score changes through a polite live region.
- Keep the board square and scaled to fit narrow screens without horizontal overflow.
- Keep directional controls large enough for comfortable touch interaction.
- Respect reduced-motion preferences; gameplay must not rely on animation to communicate state.

## Acceptance criteria

- The HTML file opens directly in a browser and works without a build step, network access, or external libraries.
- Starting a round displays a moving snake and a food item; arrow keys and WASD steer it when the board has focus.
- Directional buttons steer the snake and work on a touch-sized viewport.
- Eating food increases score and snake length; food never appears under the snake.
- Wall and self collisions reliably end the round, stop movement, and display game-over feedback.
- Pause freezes movement; resume continues the same round; starting a new round resets the current score and board.
- Direction reversal is rejected, including rapid consecutive key presses before a movement step.
- Best score survives reload when local storage is available; storage failure does not prevent play.
- Layout remains usable on desktop and mobile widths, with no horizontal page overflow.
- Other project files, games, and their storage remain unaffected.

## Verification plan

1. Open `snake-game.html` directly and test ready, start, pause, resume, and new-round states.
2. Steer with arrow keys and WASD; check that opposite-direction turns are ignored.
3. Use the directional buttons at desktop and narrow/mobile viewport sizes.
4. Eat food and verify score, growth, and non-overlapping food placement.
5. Trigger wall and self collisions and confirm movement stops and the game-over state appears.
6. Reload and confirm the best score persists without affecting other game data.
7. Verify the board and control names using the browser accessibility tree.
