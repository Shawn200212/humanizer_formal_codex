# Forward regression — 2026-08-13

Current Skill SHA-256: `D1BE6402EB2C20836BA517D9E8EAB87860FA78C74C555ADF26EA6BB44FC8B96F`

This is an instruction-level smoke test, not a Humanizer performance estimate. In one blind run:

- a bilingual `N=48` versus `N=84` conflict with no authority language returned
  `EVIDENCE BLOCKED` and `[AUTHOR DECISION]` rather than silently choosing a value;
- an already clear English paragraph returned `PRESERVE` with no unnecessary rewrite;
- a CHI Results statement claiming significance with `p=.18` and no alpha/effect contract was blocked
  before a Humanizer copyedit.

Result: **3/3 relevant cases PASS**. The required next step remains a frozen, repeated, real
source-to-revision bilingual benchmark with evaluator-only gold data and hard-gate scoring.
