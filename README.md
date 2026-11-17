# VS Code — What's New Carousel

A standalone, auto-rotating HTML carousel highlighting newer VS Code features,
built for a tradeshow booth. Single self-contained file (inline CSS + JS), no
external dependencies — works fully offline. Styled after the VS Code website
(light theme).

## Run it

Open `docs/index.html` (or `docs/vscode-whats-new-carousel.html`, an identical
copy) in any modern browser and press **F** for fullscreen.

## Slides

1. Welcome
2. Agents Window
3. Automations (in the app, and in the cloud on GitHub)
4. Agent Merge (Experimental)
5. Session Continuity (the apps in a circle, each joined to a heart in the center)
6. Continuity in Action (a recording of one session moving across the apps)
7. Copilot Harness (one harness on the Copilot SDK, Agent Host Protocol)
8. Harnesses & Models (Copilot / Claude / Codex, Copilot Fusion, bring your own key)
9. Agent Bake-Off (Compare Models, Preview)
10. Copilot Connectors (Preview)
11. Integrated Browser
12. Canvases (Preview)
13. Enterprise Ready (managed settings, sandboxing, OpenTelemetry)

One full loop takes a little over two minutes.

## Presenter controls

| Key | Action |
| --- | --- |
| `` ` `` | Toggle table-of-contents (jump to any slide) |
| `Space` | Pause / resume auto-rotation |
| `←` / `→` | Previous / next slide |
| `Home` | First slide |
| `J` | Make Blobby jump on a screenshot slide |
| `F` | Toggle fullscreen |
| `Esc` | Close the table-of-contents |

Move the mouse for a rainbow VS Code comet trail. ✨

## Media

Screenshots live in `docs/media/`, numbered in slide order. To swap one, replace
the matching file; each image is sized from its own aspect
ratio, so no code changes are needed. Three slides show a pair of screenshots
(`02-*`, `06-*`, and `11-*`).

The Continuity in Action slide plays `04-session-continuity.mp4`, one 17-second
loop recorded from the continuity animation on the code.visualstudio.com
homepage. The video restarts each time the slide appears, and the slide's
`data-duration` matches the loop length; change both together. The matching
`.png` is the poster frame shown before the video loads.

The screenshots come from the VS Code documentation, release notes, and blog on
code.visualstudio.com.

## Blobby

Blobby, the VS Code chat pet, hops between screenshot hotspots as the matching
numbered points light up, then returns to its perch. Click Blobby (or press
**J**) for a happy hop; click a screenshot to send it there. Cropped hotspots
pan into view. Tours follow each slide's existing duration and pause with
**Space** or the table of contents. Reduced motion skips hopping animations.
The continuity circle and recording retain their own animations.

The sprites in `docs/media/blobby/` are VS Code's own
animation spritesheets (MIT, see the license file in that folder), and the
keyframes in the page step through them with VS Code's frame timings.

To put Blobby on a screenshot, add `<span class="blobby POSE"></span>` inside
its `<figure class="media">`. The poses are `idle`, `love`, `cool`, `sleep`,
`typing`, `painting`, `press-button`, `clapping`, `jump`, `chef-hat`, and
`hard-hat`. Add the `eyes` class to `love`, `typing`, `painting`,
`press-button`, and `clapping`, whose sprites come without eyes.
On screenshot slides with points, give each `<li>` a `data-x` and `data-y`
hotspot (fractions from 0 to 1), a `data-pose`, and an optional zero-based
`data-img` for paired screenshots.

## Display size

The deck uses layout B: a centered VS Code wordmark, a small feature label
above larger left-hand copy, and taller screenshots bleeding off the right
edge. Screenshots are bounded by 82% of the viewport height; portrait and
paired media keep their proportions. The continuity video remains uncropped.

The layout is tuned for 16:9 displays and scales with the viewport, including
1920×1080 and 4K, without the old 1480px width cap.

The original four layout studies remain in `docs/mockups/index.html`.

## GitHub Pages

The site is published from the `docs/` folder on `main`:
<https://rwoll.github.io/vscode-whats-new-carousel/>. Keep
`docs/vscode-whats-new-carousel.html` identical to `docs/index.html`.
