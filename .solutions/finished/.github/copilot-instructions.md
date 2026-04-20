# Copilot Workspace Instructions

## Development Checklist

Before committing any changes, ensure:

- [ ] `uv run ruff check .` passes with no errors
- [ ] `uv run pytest` passes
- [ ] Code follows Python conventions (snake_case, type hints)
- [ ] No unused variables or imports

## Project Overview

**Soc Ops** is a Social Bingo game built with Python (FastAPI + Jinja2 + HTMX). Players find people who match questions to mark squares and get 5 in a row.

## Architecture

```
app/
├── templates/       # Jinja2 HTML templates
│   ├── base.html
│   ├── home.html
│   └── components/  # bingo_board, bingo_modal, game_screen, start_screen
├── static/          # CSS & JS assets
├── models.py        # Pydantic models (GameState, BingoSquare)
├── game_logic.py    # Board generation & bingo detection
├── game_service.py  # Session management (GameSession)
├── data.py          # Question bank
└── main.py          # FastAPI routes & HTMX endpoints
tests/
├── test_api.py      # API endpoint tests (httpx + TestClient)
└── test_game_logic.py  # Game logic unit tests
```

## Key Commands

```bash
uv run uvicorn app.main:app --reload --port 8000  # Run dev server
uv run pytest                                       # Run tests
uv run ruff check .                                 # Lint
```

## Styling

Uses custom CSS utility classes (Tailwind-like) in `app/static/css/app.css`:
- Layout: `.flex`, `.grid`, `.items-center`
- Spacing: `.p-4`, `.mb-2`, `.mx-auto`
- Colors: `.bg-accent`, `.bg-marked`, `.text-gray-700`

## Design Guide

When creating or updating UI, follow these design rules:

- Preserve the whimsical unicorn visual direction (pastel gradients, playful accents, celebratory tone)
- Use CSS variables in `:root` for new colors and effects before introducing new utility classes
- Prefer utility-class composition over one-off inline styles; only use inline styles for animation delays or dynamic values
- Keep typography expressive but readable: clear hierarchy for headings, medium/high contrast for body text
- Use motion intentionally: subtle sparkle/float/pulse effects, avoid excessive simultaneous animation
- Maintain mobile-first layouts; ensure controls remain tappable and readable on small screens
- Preserve existing HTMX flow and server-rendered structure in templates (`start_screen`, `game_screen`, `bingo_board`, `bingo_modal`)
- Keep accessibility in mind: retain semantic elements, descriptive labels, and sufficient contrast for interactive content
- Avoid introducing external UI frameworks or font dependencies unless explicitly requested

For major visual changes, validate both game states:
- Start screen
- Active game with marked/winning squares and bingo modal

## State Management

- `GameSession` manages game state server-side
- State persisted via signed cookies (itsdangerous)
- HTMX handles partial page updates without full reloads
