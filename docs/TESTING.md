# Testing and release verification

Use the SFHS checkout pinned by `one-shot/SFHS-PIN.json`; do not install or publish a replacement runtime from this repository. From that toolchain root, materialize the game repository and use the generated `.sfhs-grad-skyline-drop-*` project path:

```text
pnpm install --frozen-lockfile
pnpm sfhs one-shot graduate materialize --project <skyline-drop-path> --json
pnpm sfhs inspect --project <materialized-path> --json
pnpm sfhs validate --project <materialized-path> --json
pnpm sfhs check --project <materialized-path> --changed src --json
pnpm sfhs pack --project <materialized-path> --json
pnpm sfhs verify --project <materialized-path> --json
pnpm --dir <materialized-path> run test
pnpm --dir <materialized-path> run test:browser:canonical
```

The browser smoke must exercise boot, semantic placement, pause/resume, resize, and absence of runtime external requests. Preserve its JSON result with the current artifact. The CI workflow reproduces these gates on pull requests and `main`; only `main` may deploy Pages.

Physical acceptance is separate: use `one-shot/GRADUATION-PHYSICAL-TEST-SEED.json` generated for the exact artifact. A desktop or emulator result cannot substitute for Samsung Galaxy S21 Ultra / stable Android Chrome evidence.
