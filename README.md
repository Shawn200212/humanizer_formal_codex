# Humanizer Formal

**English**

Chinese and English academic copyediting for research papers, theses, abstracts and reviewer
responses. The focus is understandable scholarly meaning, evidence-faithful claims and a
recognizable author voice—not a generic “human” style.

This repository was renamed from `Shawn200212/humanizer_codex` in September 2026. Its history
is retained. Installable source is in the private
[humanizer_formal_codex-core](https://github.com/Shawn200212/humanizer_formal_codex-core) repository.
The UI display name is `humanizer_formal`; the validated Codex invocation is `$humanizer-formal`.

**中文**

负责中英文学术论文、学位论文、摘要和审稿回复的润色。重点是把研究真正想表达的内容写清楚，
而不是增加“学术感”、套用同一种句式，或追求检测器分数。

本仓库由 `humanizer_codex` 改名，原有历史保留。完整源码在私有
[humanizer_formal_codex-core](https://github.com/Shawn200212/humanizer_formal_codex-core)。
界面显示 `humanizer_formal`，实际入口为 `$humanizer-formal`。

## Scope / 两个版本的分工

**English**

The formal edition addresses unclear referents, logical scope, comparisons, evidence-to-claim
relationships and bilingual inconsistencies. It distinguishes language repair from an author
decision or a missing piece of evidence. It does not supply unreported findings or promise
publication, authorship certification or detector evasion.

For public-facing website copy, news/broadcast scripts and everyday explanations, see
[Humanizer Informal](https://github.com/Shawn200212/humanizer_informal_codex).
A research project website does not automatically need academic-paper prose.

**中文**

学术版关注句意消歧、限定范围、比较关系、证据强度和中英文含义一致性。
需要作者确认的意思与缺少证据的主张，不能靠润色偷偷补齐。

网站介绍、新闻播报和日常阐释请用
[Humanizer Informal](https://github.com/Shawn200212/humanizer_informal_codex)。
介绍研究项目的网站，也不必写成论文。

## What is public / 公开边界与结果解释

**English**

Only overview documentation, bibliographic metadata and bounded aggregate evaluation information
are published here. Skill instructions, helper source, paper abstracts/full text, model artifacts,
internal cases and user drafts are not published. The public overview is not an installable skill.

See [the September revision summary](reports/2026-09-13-revision.md) for current validation.
Existing `data/`, `gallery/` and August training/forward-test reports describe the earlier
abstract-corpus experiment. Its dated synthetic-filler classification metrics are **not** scores
for either current editor. No language model was fine-tuned for this release.

**中文**

本仓库只公开说明、文献元数据及有限的评估摘要，不提供可安装的 skill，
不公开内部规则、辅助脚本、论文摘要/全文、模型文件、内部用例或用户原稿。

当前验证见 [2026-09-13 修订说明](reports/2026-09-13-revision.md)。
原有数据、图表和八月报告属于历史摘要语料实验；其中的分类准确率不代表本次润色质量。
本次没有微调语言模型，也不承诺所有文本都无歧义或绝不过拟合。

## Licensing / 许可

**English**

Repository prose and private skill source remain all rights reserved; see [LICENSE](LICENSE).
Public aggregate measurements and CC0-derived bibliographic metadata in `data/` retain the
separate terms in [LICENSE-DATA](LICENSE-DATA). Underlying papers retain their own rights.

**中文**

仓库说明文字和私有 Skill 源码保留全部权利，见 [LICENSE](LICENSE)。公开的聚合测量结果和 CC0 来源的书目元数据适用 [LICENSE-DATA](LICENSE-DATA) 中的单独条款；原始论文的权利仍归各自权利人所有。
