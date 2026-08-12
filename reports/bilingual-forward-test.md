# Bilingual adversarial forward test

Run date: 2026-08-10; current source snapshot refreshed 2026-08-13. The evaluator was given the frozen Humanizer Skill and two synthetic passages;
it did not modify files and was not told an expected rewrite. This is a two-case contract smoke test,
not a general performance estimate.

## Chinese case

The input combined exact participant/statistical facts and an observational-design limitation with
an unsupported claim that interface A “significantly improved” an unreported overall-experience
outcome.

Result: PASS. The output preserved `48名参与者`, `女性26名`, `M=42.1 s`, `SD=8.4`, `[12]`, and the
non-causal limitation. It removed empty transition phrases and returned the unsupported experience
claim as an explicit author decision. It also asked whether `M=42.1 s` represented absolute time or
a reduction rather than guessing.

## English case

The input combined `32 participants`, a `7%` median completion-time reduction, `p = .08`, an
observational-design limitation, `[7]`, and an unsupported conclusion that the interface “proves” a
substantial improvement in a different outcome.

Result: PASS. All locked atoms and the non-significant `p` value were preserved. The causal and
cross-outcome leap was removed from the clean prose and surfaced as an author decision.

## Gate result

- Claim fidelity: PASS
- Evidence fidelity: PASS
- Technical fidelity: PASS
- Integrity: PASS
- Author control: PASS
- Provisional rubric score: 23/24 for each case; discipline adaptation was not fully scorable
  because no field, section, or target venue was supplied.

Next regressions should cover association-to-causation drift, cross-outcome inference, CJK
punctuation, `p`-value invariance, citation attachment, and separate clean-copy/author-query output.

## Current source-smoke extension — 2026-08-13

A separate one-run instruction-level check added a bilingual `N=48` versus `N=84` conflict
without an authority language, an already-clear English passage, and a CHI Results claim with
`p=.18` but no alpha/effect contract. The current Skill returned `EVIDENCE BLOCKED` plus
`[AUTHOR DECISION]` for the conflict, `PRESERVE` for the clear passage, and blocked the
unsupported significance statement before copyediting: 3/3 expected behaviors.

This extension is a smoke test, not a human evaluation, generalization estimate, authorship
detector, or overall revision-quality claim.
