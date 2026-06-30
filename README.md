# VS Code — What's New Carousel

A standalone, auto-rotating HTML carousel highlighting newer VS Code features,
built for a tradeshow booth. Single self-contained file (inline CSS + JS), no
external dependencies — works fully offline. Styled after the VS Code website
(light theme).

## Run it

Open `public/index.html` (or `public/vscode-whats-new-carousel.html`) in any modern browser
and press **F** for fullscreen.

## Slides

1. Agents Window
2. Bring your own harness (Copilot / Claude / Codex)
3. Bring your own key (incl. air-gapped / local Ollama)
4. OpenTelemetry (fleet trajectories & usage)
5. Integrated Browser (point-and-click feedback)
6. Unified Sessions (local + GitHub Cloud, with steering)
7. Control from your phone (`insiders.vscode.dev/agents`)

## Presenter controls

| Key | Action |
| --- | --- |
| `` ` `` | Toggle table-of-contents (jump to any slide) |
| `Space` | Pause / resume auto-rotation |
| `←` / `→` | Previous / next slide |
| `Home` | First slide |
| `F` | Toggle fullscreen |
| `Esc` | Close the table-of-contents |

Move the mouse for a rainbow VS Code comet trail. ✨

## Media

Screenshots live in `public/media/`. To swap one, replace the matching file (the
phone slide uses a portrait screenshot rendered inside an iPhone frame).

## GitHub Pages

Site assets live under `public/`. Configure Pages to serve from that folder
(e.g. a workflow that publishes `public/`, or set the Pages source accordingly).
