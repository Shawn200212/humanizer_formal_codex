# Historical method record — August 2026

This document preserves the August 13 public method snapshot, including its dated aggregate
measurements. It is not a benchmark for the September editorial workflow. Current scope and
bounded tests are in [the September revision summary](../reports/2026-09-13-revision.md).

# Method and interpretation boundaries

## Revision contract

Humanizer uses an evidence lock before revising. Numbers, units, citations, quotations, named
entities, negation, uncertainty, comparison classes, and claim force are immutable unless the
author explicitly supplies corrected evidence. A polished sentence is rejected if it silently
changes any of those atoms. Ambiguous or contradictory source claims are surfaced as author
decisions rather than “fixed” by invention.

The workflow does not optimize for AI-detector scores and does not claim that any passage is human-
or machine-authored.

## Corpus boundary

The current source snapshot, dated 2026-08-13, uses a deterministic OpenAlex snapshot with 100 Chinese and 100 English records. The
paper—not the extracted sentence—is the split unit, preventing a paper from appearing in more than
one of train/development/test. The builder balances broad fields and unique venues when possible.

This is a broad research snapshot, not an exhaustive traversal of the web or a certified ranking
of “mainstream” venues. OpenAlex metadata is CC0, but linked article content has separate rights.
The public repository exposes only bibliographic metadata and hashes. A future full-text release
requires article-level license evidence, attribution, retraction checks, and a new versioned lock.

## Optimization and early stopping

Deterministic rules insert generic filler around authentic abstract sentences. A hashed character
n-gram logistic classifier learns this narrow distinction. Learning rate and regularization are
chosen by development loss. The classification threshold is chosen by development balanced
accuracy. The fixed test set is evaluated only after both choices are frozen.

With a maximum of 2,000 epochs and patience 50, development loss reached its minimum at epoch 485.
Training stopped at epoch 535 and restored epoch 485. The rising development loss after the minimum
is the observed onset of overfitting for this synthetic diagnostic.

## Valid claim

The frozen model achieved 0.9371 balanced accuracy on 334 synthetic test sentences. This supports
only the statement that the bundled diagnostic separates its authentic-abstract sentences from its
deterministically inserted filler on this fixed snapshot. It cannot establish authorship, factual
correctness, general revision quality, or publication outcomes.
