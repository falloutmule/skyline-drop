# Repository graduation record

## Operating context

| Field | Resolved value |
| --- | --- |
| Project root | `skyline-drop/` |
| Intended repository | `falloutmule/skyline-drop` |
| Canonical branch | `main` |
| External SFHS | `falloutmule/single-file-html-software@4248c67021e930b7fb4a882f73dfd8ab87df0ee7` |
| Adapter | Pixi v8 |
| Primary target | Samsung Galaxy S21 Ultra / stable Android Chrome |
| Secondary target | Desktop Chromium |

The source was imported from the preserved Skyline Drop SFHS worktree using the current graduation `inspect`, `plan`, and transactional `import` commands. The original shared SFHS worktree contained unrelated user work and was not changed.

## Source authority

| Path or object | Classification | Authority basis | Current status | Relationship to canonical source | Action |
| --- | --- | --- | --- | --- | --- |
| `src/`, `public/`, `tests/`, `sfhs.project.json` | Editable source | Explicit SFHS manifest, validated graduation lineage, and matching canonical build | VERIFIED | Authoritative source | Retained at repository root. |
| `dist/index.html` | Generated artifact | Produced only by the pinned SFHS packer and exact verifier | VERIFIED | Canonical output; ignored working artifact | Regenerate; never hand-edit or commit. |
| `historical/candidate/` | Legacy candidate | Preserved pre-graduation input | SUPERSEDED | Historical only | Retained outside editable/release paths. |
| `evidence/milestones/legacy-repairs/` | Milestone evidence | Existing focused repair records | VERIFIED / historical | Supports retained behavior claims | Consolidated without deletion. |
| Prior one-shot physical report | Device evidence | User-authored reported pass bound to exact current artifact bytes | REPORTED | Evidence detail, not independent verification | Retained in `one-shot/`. |

## Migration and cleanup plan executed

- Preserve editable source, tests, historical handoff/decision material, milestone evidence, and artifact-bound physical report.
- Import source transactionally; keep SFHS external and pinned rather than copy framework source.
- Move legacy candidate to `historical/candidate/` and consolidate scattered repair proof under `evidence/milestones/legacy-repairs/`.
- Add repository front-door documentation, rights statement, source/evidence guide, CI, and an action-based Pages deployment workflow.
- Regenerate `dist/index.html` only through SFHS; retain current exact proof under `evidence/current/`.
- Rollback is a normal Git revert of the graduation commit; the source handoff remains in its original preserved worktree and Git history.

No stale evidence was deleted: there is not yet a second newer canonical generation in this repository and the retained milestone records have unique explanatory value.
