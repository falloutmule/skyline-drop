# Skyline Drop

**Skyline Drop** is a short portrait-first isometric city-building puzzle: place, rotate, inspect, remix, and drop districts so homes and shops connect to both roads and underground utilities.

Play: https://falloutmule.github.io/skyline-drop/

Current status: canonical desktop verification is being regenerated from the imported SFHS source. The prior device result is retained as **reported**, not independently verified, and applies only to the previous artifact described in [PROJECT-STATUS.md](docs/PROJECT-STATUS.md).

## Play

Skyline Drop is designed for portrait mobile play in stable Android Chrome and is also checked in desktop Chromium. It has three constrained levels. Complete each by connecting residents and jobs to the road entrance and utility hub, then choose a persistent upgrade.

Controls: Arrow keys/WASD move; Q/E rotate; M remix the current eligible district; Space drops; X toggles surface/underground; R restarts; Escape pauses. Touch controls expose the same actions, and the information panel responds to board taps.

Implemented: surface and underground planning, connected roads and utilities, authored Road Remix layouts, shared-road ownership, utility overlap, inspection, touch controls, fullscreen, pause/restart/progression, three levels, and a Pixi/WebGL presentation.

Known limitation: a new canonical build still needs a fresh artifact-bound Samsung Galaxy S21 Ultra session. No automated browser result is presented as physical-device acceptance.

## Source, artifact, and verification

`src/` is the authoritative editable game source; `public/` owns local assets; `sfhs.project.json` declares the Pixi v8 contract. `dist/index.html` is the disposable canonical output produced only by the pinned SFHS toolchain in `one-shot/SFHS-PIN.json`. `historical/candidate/` is a preserved legacy candidate, never release input.

The repository deliberately uses SFHS as an external pinned toolchain rather than vendoring the framework. See [ARCHITECTURE.md](docs/ARCHITECTURE.md) and [TESTING.md](docs/TESTING.md) for the local materialization, validation, packing, verification, browser, and Pages paths.

Current artifact: `skyline-drop-cfb081a04f41`; `dist/index.html`; 2,091,772 bytes; SHA-256 `d7e95638ad9d31e924fbf9ba9d8f4d95070d06a57b4ade461a2c42ab1f726721`; verified 2026-08-06. The Pages URL is recorded here only after deployed-byte parity is checked.

## Development

Use Node 24+ and pnpm 11.9+ with a clean checkout of the SFHS commit pinned in `one-shot/SFHS-PIN.json`. Materialize this repository into that checkout, then run the SFHS commands from the toolchain workspace. Exact commands and the CI-equivalent sequence are in [TESTING.md](docs/TESTING.md).

Project details: [game specification](docs/GAME-SPEC.md), [status](docs/PROJECT-STATUS.md), [roadmap](docs/ROADMAP.md), [architecture](docs/ARCHITECTURE.md), [testing](docs/TESTING.md), [decisions](docs/DECISIONS.md), and [rights](RIGHTS.md).
