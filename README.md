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

## Speaker notes on phone

When hosting on GitHub Pages (e.g. `https://lizell.github.io/chrillo-reveals/`):

1. Open the presentation URL on your laptop
2. On your phone (same WiFi), open the same URL with `?view=speaker` appended, e.g.
   `https://lizell.github.io/chrillo-reveals/?view=speaker`

Note: slides are **not synced** between devices in this mode. For synced control you would need the [multiplex plugin](https://revealjs.com/multiplex/) with a socket.io server.

### Local network alternative

```bash
npm run dev -- --host 0.0.0.0
```

Then on your phone, go to `http://<your-ip>:1948/<presentation>.md?view=speaker`.

## Adding a new presentation

1. Create a new `.md` file in `slides/`
2. Use `---` for horizontal slides and `--` for vertical slides
3. Put images in `slides/assets/images/`
4. Run `npm run dev` — the index page lists all presentations
