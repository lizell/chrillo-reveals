# chrillo-reveals

Presentations by Chrille, powered by [reveal-md](https://github.com/webpro/reveal-md).

**Live:** https://lizell.github.io/chrillo-reveals/

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

## Code Base · Järvsö 2026

Presentation för lördagen den 19 september: **Kom igång med AI i utvecklingsarbetet – så här gjorde vi på SVT**.

- [Presentationens källfil](slides/code-base-2026.md): 25 huvudbilder, 2 valbara introduktionsbilder om Christian och Athega, 7 vertikala fördjupningar om Ossy, Login och Astrid samt ett valbart Dialora-exempel, 11 begreppsbilder, 11 tipsbilder, 3 reservbilder och talaranteckningar.
- [Körschema och praktiska instruktioner](workshops/code-base-2026/README.md): 40 minuter inklusive övningar + 5 minuter frågor.
- [Deltagarblad](workshops/code-base-2026/deltagarblad.md): promptmall, reviewstöd och första försöket.
- [Begrepp och praktiska tips](workshops/code-base-2026/fordjupning.md).
- [Källor och avgränsningar](workshops/code-base-2026/kallor.md).

Kör `npm run dev` och välj `code-base-2026.md`. Efter `npm run build` finns presentationen i `docs/code-base-2026.html` och på den lokala startsidan. Publicering sker separat.
