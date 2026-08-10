# Humanizer optimization report

The frozen model is a narrow generic-filler diagnostic, not an AI detector. Hyperparameters and the decision threshold were selected without consulting the test split.

## Early stopping

- Selected learning rate: 0.3
- Selected L2: 0.0
- Best development epoch: 365
- Diagnostic stop epoch after patience: 415
- Restored checkpoint: epoch 365
- Development loss at checkpoint: 0.553156

## Frozen test

- Balanced accuracy: 0.9701
- Authentic-sentence F1: 0.9691
- Filler-sentence F1: 0.9709
- Binary cross-entropy: 0.5028

## Interpretation

The curve is evidence only for the bundled synthetic task. It cannot establish human authorship, detect model use, measure factual fidelity, or predict acceptance. Human review and the evidence-lock protocol remain mandatory.
