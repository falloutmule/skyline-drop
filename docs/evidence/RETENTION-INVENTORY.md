# Evidence retention inventory

| Item | Build/source identity | Status | Retention action | Successor |
| --- | --- | --- | --- | --- |
| Legacy candidate and its scripts | Pre-graduation candidate | SUPERSEDED | Retained in `historical/candidate/` because it explains the migration boundary; never deployable. | SFHS canonical output. |
| Legacy repair screenshots, smoke JSON, and focused logs | Historical repair milestones | VERIFIED / historical | Consolidated in `evidence/milestones/legacy-repairs/`; they document still-relevant road, remix, utility, and inspection behavior. | Current canonical evidence when regenerated. |
| Prior canonical report | `skyline-drop-cfb081a04f41` | SUPERSEDED | Retained in `one-shot/VERIFICATION-REPORT.md` and physical report because it is the only reported Samsung result. | `evidence/current/` current release record. |
| Current canonical verifier and browser proof | `skyline-drop-cfb081a04f41` | VERIFIED | Retained in `evidence/current/`; this graduation reproduced the prior canonical artifact exactly. | N/A |

No heavy evidence was deleted in this migration: the available legacy records remain relevant milestones and there is not yet a second newer canonical generation from this repository. Future releases retain the current and immediately previous canonical generations, retain lightweight manifests and unique physical evidence, and remove only redundant material with a verified successor and no live reference.
