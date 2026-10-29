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

- [Presentationens källfil](slides/code-base-2026.md): 25 huvudbilder, 3 valbara introduktionsbilder om Christian och Athega, 7 vertikala fördjupningar om Ossy, Login och Astrid samt ett valbart Dialora-exempel, 11 begreppsbilder, 11 tipsbilder, 4 valbara demobilder i slutet, 3 reservbilder och talaranteckningar.
- [Körschema och praktiska instruktioner](workshops/code-base-2026/README.md): 40 minuter inklusive övningar + 5 minuter frågor.
- [Deltagarblad](workshops/code-base-2026/deltagarblad.md): promptmall, reviewstöd och första försöket.
- [Begrepp och praktiska tips](workshops/code-base-2026/fordjupning.md).
- [Källor och avgränsningar](workshops/code-base-2026/kallor.md).

Kör `npm run dev` och välj `code-base-2026.md`. Efter `npm run build` finns presentationen i `docs/code-base-2026.html` och på den lokala startsidan. Publicering sker separat.

## eXtreme Collaboration · 30 October 2026

[When agents write the code, what do we do together?](slides/xcc-2026.md) — a 10-minute English talk, with ten slides and timed speaker notes. The SVT login story spans three slides, followed by a short colleague reaction from another thread.

Run `npm run dev` and select `xcc-2026.md`, or build and open `docs/xcc-2026.html` through a local HTTP server. Press `S` for speaker notes. Images and diagrams are local. A [PDF backup](docs/xcc-2026.pdf) is included; regenerate it after slide changes.

The English conversation screenshots in `slides/assets/images/xcc-2026/` are AI-assisted translated recreations of the anonymized Code Base assets; the Swedish originals are preserved. The embedded product UI and the results image remain Swedish. Read the translated images as illustrations of the conversation, not pixel-exact evidence of the product. No new test run or production verification of SVT login is implied.

Paris inspiration: Plaud recording **10-28 OpenAI dev day Paris**, 54:02 (verifiable goals), 3:13:59 (making implicit team knowledge available). XCC context: https://xcc.agical.se/om-xc26/ and https://xcc.agical.se/program/.

Slide 4 uses an AI-generated illustrative workshop scene (`workshop-candid.png`): five adults working with cardboard and paper prototypes. It is labelled on the slide and does not depict a real workshop or the SVT team. Earlier sourced photo alternatives are retained in the assets folder.
