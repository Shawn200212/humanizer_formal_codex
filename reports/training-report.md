# Humanizer current source-snapshot optimization report

The frozen model is a narrow generic-filler diagnostic, not an AI detector. Hyperparameters and the decision threshold were selected without consulting the test split.

## Early stopping

- Selected learning rate: 0.3
- Selected L2: 0.0
- Best development epoch: 485
- Diagnostic stop epoch after patience: 535
- Restored checkpoint: epoch 485
- Development loss at checkpoint: 0.567742

## Frozen test

- Balanced accuracy: 0.9371
- Authentic-sentence F1: 0.9329
- Filler-sentence F1: 0.9408
- Binary cross-entropy: 0.4974

## Interpretation

The curve is evidence only for the bundled synthetic task. It cannot establish human authorship, detect model use, measure factual fidelity, or predict acceptance. Human review and the evidence-lock protocol remain mandatory.

This current snapshot also passed a three-case instruction-level smoke test: conflicting bilingual
counts were blocked, clear prose was preserved, and an unsupported significance claim was blocked.
That 3/3 result is a contract check, not a generalization or revision-quality estimate.
