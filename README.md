<div align="center">

# SudokuGame - Sudoku

**Sudoku («Судоку») in a single HTML page: four levels by solving technique, hints that explain the technique, notes, pause and records. It runs in the browser with no server and no internet: open `index.html` or play it online.**

[**▶ Play online →**](https://alexalesha.github.io/SudokuGame/) &nbsp;·&nbsp; [Русская версия этого файла](README.ru.md)

[![Status](https://img.shields.io/badge/status-stable-brightgreen)](#) [![CI](https://github.com/ALEXalesha/SudokuGame/actions/workflows/ci.yml/badge.svg)](https://github.com/ALEXalesha/SudokuGame/actions/workflows/ci.yml) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE) [![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML) [![Website](https://img.shields.io/badge/Website-open-0A84FF?logo=googlechrome&logoColor=white)](https://alexalesha.github.io/SudokuGame/) [![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=claude&logoColor=white)](https://claude.com/claude-code)

Code, tests and docs are written by Claude (Anthropic) in Claude Code. Ideas, testing and decisions - Alexey.

</div>

The interface is in Russian.

![Menu](docs/screens/menu.png)

![A hard puzzle with notes](docs/screens/play.png)

![Levels](docs/screens/levels.png)

## What is in the game

- Puzzles are generated in the page; a bitmask solver checks that the solution is unique, a logical solver rates the level by human techniques.
- Levels: Easy (last candidate, single in a box), Medium (hidden singles), Hard (intersections, pairs), Expert (triples, X-wing, wings).
- A hint places one digit and explains the technique; if there is a mistake on the board, it shows it first.
- Notes and auto-notes, undo and redo, a daily puzzle shared by everyone that day, records per level, gamepad support.

## Controls

| Key | Action |
|---|---|
| Click or arrows, then a digit | fill a cell |
| N / Q | notes / auto-notes |
| Backspace | erase |
| Ctrl+Z / Ctrl+Y | undo / redo |
| H | hint |

Keys can be changed in the settings where the game offers it; a gamepad works too where noted above.

## Run locally

Open `index.html` in Chrome, Edge or Firefox. Everything is in the repository; nothing is downloaded.

## Tests

The laws are Playwright tests in `tests/`. They open the page by its file address in headless
Chromium, one at a time:

```
npm install
npx playwright install chromium
npm test
```

Mouse capture in the tests is always a stub (a real `requestPointerLock` in headless Chromium on
Windows can clip the user's cursor).
The pictures above were made headless by the screenshot script of the Hub collection.

## History

The game was made in the [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io) collection (folder `web/sudoku`), where it also runs in the Hub ([play there](https://alexalesha.github.io/)). This repository carries the game with its commit history.

## Licence

MIT, see [LICENSE](LICENSE).
