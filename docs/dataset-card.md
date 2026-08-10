# Corpus and evaluation card

## Intended use

The corpus provides aggregate bilingual academic-style observations and a reproducible synthetic generic-filler diagnostic. It supports editing research and Skill regression tests. It is not an authorship detector, a plagiarism corpus, a venue-ranking dataset, or evidence that a passage was written by a person or a model.

## Composition

- 200 paper records: 100 Chinese-language and 100 English-language records.
- Deterministic language-stratified split: 70 train, 15 development, and 15 test records per language.
- Journal articles plus conference papers where reliable records pass the language and venue filters.
- At most one selected record per normalized venue when the source pool permits, with field-balanced round-robin selection.
- Stored content is bibliographic metadata and abstract text; full-paper PDFs are not downloaded or redistributed.

Exact counts, source snapshot time, field coverage, hashes, and license fields are generated in `data/dataset_manifest.json`.

## Source and licensing

Records are retrieved from OpenAlex. OpenAlex publishes its metadata under CC0. Each record preserves the OpenAlex identifier, DOI when available, venue, source URL, retrieval time, and the content-license value reported for the best open location. OpenAlex does not grant rights to linked PDFs; this project therefore does not bundle those files.

## Selection

The builder requests open records with abstracts, filters Chinese and English using script-aware thresholds, rejects very short abstracts and missing venues, deduplicates identifiers, prioritizes curated/core sources and citations, then balances domains and venue types. “Representative” does not mean exhaustive or equivalent to commercial journal rankings.

## Synthetic task

Training inserts split-specific generic filler sentences around authentic abstract sentences. A hashed character n-gram logistic model learns to flag the inserted sentences. Hyperparameters are selected only on the development split. Training uses patience-based early stopping and restores the best development-loss checkpoint. The test split is evaluated once after selection.

## Known limitations

- Database language labels can be wrong; script-aware filtering reduces but cannot eliminate this error.
- Abstracts do not represent every section or discipline.
- Synthetic filler is narrower than real revision problems.
- Citation count and `is_core` are sampling aids, not quality judgments.
- Conference coverage, especially Chinese-language coverage, is thinner than journal coverage.
- Performance cannot be generalized to AI detection, authorship attribution, or acceptance outcomes.

## Reproduction

Run, in order:

```text
python scripts/build_corpus.py
python scripts/train_early_stop.py
python scripts/plot_training_curve.py
```

Set `OPENALEX_API_KEY` when the current API policy requires authentication. Never commit an API key.
