# Product Requirements Document: Dark Theme

## Overview

Add an optional dark theme to the existing standalone Memory Game. Players can switch between the current light appearance and a dark appearance without changing how the game is played.

## Problem

The game currently has only a light color palette. Players who prefer a darker interface, including when playing in low-light environments, have no way to change it.

## Goals

- Offer a clear, accessible control to switch between light and dark themes.
- Keep text and interactive elements readable in both themes.
- Remember the player's theme choice between visits when browser storage is available.
- Preserve existing gameplay, layout, and score behavior.
- Keep the game self-contained, responsive, and free of new dependencies.

## Out of scope

- Automatically selecting a theme from the operating system.
- Adding more themes or user-configurable colors.
- Changing game rules, card symbols, grid sizes, ratings, or score ranking.

## User experience

- The current light theme remains the default for players with no saved preference.
- A theme toggle is available on the game page and can be operated by mouse or keyboard.
- The control communicates the current theme and the action that will happen when activated.
- The selected theme applies immediately and is restored on subsequent visits when local storage is available.
- Theme changes do not reset the board, moves, timer, rating, or saved scores.

## Functional requirements

1. Add a theme control with an accessible name and state; expose whether dark mode is active using an appropriate ARIA attribute.
2. Toggle the page between light and dark color palettes without reloading.
3. Persist the selected theme under a theme-specific local-storage key. Do not overwrite or repurpose the existing best-score data.
4. If no valid saved theme is present, start in the existing light theme.
5. Apply the theme consistently to the page background, text, buttons, game cards, controls, score panel, and win dialog.
6. Keep all existing game behavior and both grid sizes operational.

## Accessibility and visual requirements

- Maintain visible keyboard focus on the theme control and cards.
- Use readable foreground/background combinations in both themes, targeting WCAG 2.1 AA contrast for normal text (4.5:1) and large text (3:1).
- Preserve card flip animations, responsive layouts, and existing keyboard interaction.
- The toggle's accessible name and pressed state must accurately describe the current theme.

## Acceptance criteria

- A first-time visit displays the existing light theme.
- Activating the theme control switches all relevant surfaces to dark colors immediately; activating it again restores the light colors.
- The theme control works with keyboard focus and Enter/Space, and exposes its current state to assistive technology.
- Reloading the page restores the last selected theme when browser local storage is available.
- Changing themes during a game does not reset or alter cards, moves, timer, rating, matched pairs, or best scores.
- Both 4×4 and 6×6 games can still be played to completion, including the win dialog and Play Again action, in either theme.
- Existing keyboard/mouse card controls, responsive layout, and best-score display continue to work.
- No external dependency or build step is introduced.

## Verification plan

1. Open `memory-game.html`; confirm the light theme and existing layout are unchanged initially.
2. Toggle dark mode, inspect the page, controls, cards, best scores, and win dialog for readable colors.
3. Toggle back to light mode and confirm it matches the existing appearance.
4. Select each grid size and play a few turns in both themes; complete a game and use Play Again.
5. Reload after selecting each theme and confirm the choice persists without affecting saved scores.
6. Use Tab and Enter/Space to reach and operate the theme control and to play cards.
7. Check the layout at desktop and narrow/mobile viewport widths.
