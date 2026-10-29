[English](README.md) | [简体中文](README.zh-CN.md)

<a id="humanizer-formal"></a>

# Humanizer Formal

Chinese and English academic copyediting for research papers, theses, abstracts and reviewer
responses. The focus is understandable scholarly meaning, evidence-faithful claims and a
recognizable author voice—not a generic “human” style.

This repository was renamed from `Shawn200212/humanizer_codex` in September 2026. Its history
is retained. Installable source is in the private
[humanizer_formal_codex-core](https://github.com/Shawn200212/humanizer_formal_codex-core) repository.
The UI display name is `humanizer_formal`; the validated Codex invocation is `$humanizer-formal`.

<a id="scope--两个版本的分工"></a>
<a id="scope"></a>
<a id="两个版本的分工"></a>

## Scope

The formal edition addresses unclear referents, logical scope, comparisons, evidence-to-claim
relationships and bilingual inconsistencies. It distinguishes language repair from an author
decision or a missing piece of evidence. It does not supply unreported findings or promise
publication, authorship certification or detector evasion.

For public-facing website copy, news/broadcast scripts and everyday explanations, see
[Humanizer Informal](https://github.com/Shawn200212/humanizer_informal_codex).
A research project website does not automatically need academic-paper prose.

<a id="what-is-public--公开边界与结果解释"></a>
<a id="what-is-public"></a>
<a id="公开边界与结果解释"></a>

## What is public

Only overview documentation, bibliographic metadata and bounded aggregate evaluation information
are published here. Skill instructions, helper source, paper abstracts/full text, model artifacts,
internal cases and user drafts are not published. The public overview is not an installable skill.

See [the September revision summary](reports/2026-09-13-revision.md) for current validation.
Existing `data/`, `gallery/` and August training/forward-test reports describe the earlier
abstract-corpus experiment. Its dated synthetic-filler classification metrics are **not** scores
for either current editor. No language model was fine-tuned for this release.

<a id="licensing--许可"></a>
<a id="licensing"></a>
<a id="许可"></a>

## Licensing

Repository prose and private skill source remain all rights reserved; see [LICENSE](LICENSE).
Public aggregate measurements and CC0-derived bibliographic metadata in `data/` retain the
separate terms in [LICENSE-DATA](LICENSE-DATA). Underlying papers retain their own rights.
