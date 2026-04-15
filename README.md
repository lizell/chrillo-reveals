# chrillo-reveals

Presentations by Chrille, powered by [reveal-md](https://github.com/webpro/reveal-md).

## Setup

```bash
npm install
```

## Development

```bash
npm run dev
```

Opens a live-reload server. Edit any `.md` file and the presentation updates instantly.

## Build

```bash
npm run build
```

Generates a static site in `docs/`. This also runs automatically as a pre-commit hook.

## Presentation controls

| Key | Action |
|---|---|
| `→` / `↓` | Next slide (horizontal / vertical) |
| `←` / `↑` | Previous slide |
| `S` | Speaker notes (popup window) |
| `O` | Overview mode |
| `F` | Fullscreen |
| `Esc` | Exit overview / fullscreen |

## Speaker notes

Press `S` during a presentation to open the speaker view in a popup window.
It shows your notes, a preview of the next slide, and a timer.

## Adding a new presentation

1. Create a new `.md` file in `slides/`
2. Use `---` for horizontal slides and `--` for vertical slides
3. Put images in `slides/assets/images/`
4. Run `npm run dev` — the index page lists all presentations
