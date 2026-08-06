# Architecture

The authoritative source is `src/`; `public/assets/` provides local artwork; `sfhs.project.json` selects the Pixi v8 lane and canonical `dist/index.html` output. The retained candidate is isolated under `historical/candidate/` and is not editable or release input.

`input.ts` turns DOM/keyboard/touch events into semantic actions. `simulation.ts`, `state.ts`, `levels.ts`, and `pieces.ts` own deterministic state transitions and rules. `presentation.ts` reads state into Pixi visuals; `main.ts` wires the SFHS Pixi adapter/runtime, DOM controls, lifecycle, and diagnostics. Rendering does not mutate game state.

The exact external SFHS toolchain commit and linked workspace packages are pinned in `one-shot/SFHS-PIN.json`. SFHS materializes a disposable overlay with workspace links, packs `dist/index.html`, verifies its byte identity, and runs the canonical Chromium smoke. GitHub Actions repeats that path in a temporary checkout, uploads only the verified HTML and `.nojekyll`, and deploys it through GitHub Pages.
