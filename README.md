# Beautimeter Research Skill / Beautimeter 研究版 Skill

## 中文

依据 **Bin Jiang 教授的 Beautimeter 论文及其提供的原始 GPT 指令**整理的可迁移研究版 skill。使用 Christopher Alexander 的活力结构十五项属性比较两张图片，每项计 0–1 分，每张图合计 0–15 分；默认只返回两个总分。

本 skill 不固定模型，不包含 API 密钥，也不依赖原 GPT 的分享链接。不同模型、API 服务及运行条件可能产生不同分数；这是研究版实现，不是原 GPT 的导出副本或经过验证的客观美度量表。

### 使用

在 Codex 中安装：

```powershell
git clone https://github.com/eleanor-wsyy/beautimeter-research-skill.git "$HOME/.codex/skills/beautimeter-skill"
```

在新对话中依次上传两张图片，输入：

```text
用 $beautimeter-skill 给这两张图打分，只显示两个总分。
```

其他支持图片理解的 AI 环境可直接使用 [SKILL.md](SKILL.md) 中的评分指令。仓库是指令包，不是打开链接即可评分的网页。

## English

A portable research skill based on **Professor Bin Jiang’s Beautimeter paper and the original GPT instructions he shared**. It compares two images using Christopher Alexander’s fifteen properties of living structure. Each property is scored from 0 to 1, giving each image a total from 0 to 15. By default, it returns only the two totals.

The skill does not fix a model, include an API key, or depend on the original GPT’s sharing link. Scores may vary across models, API services, and runtime conditions. This is a research implementation, not an exported copy of the original GPT or a validated objective measure of beauty.

### Usage

Install in Codex:

```sh
git clone https://github.com/eleanor-wsyy/beautimeter-research-skill.git "$HOME/.codex/skills/beautimeter-skill"
```

In a new conversation, attach two images in order and ask:

```text
Use $beautimeter-skill to score these two images; show only the two totals.
```

For other vision-capable AI environments, use the scoring instructions in [SKILL.md](SKILL.md). This repository is an instruction package, not a hosted image-scoring website.

## 来源与文件 / Sources and files

- **Method / 方法:** Bin Jiang, *Beautimeter: Harnessing GPT for Assessing Architectural and Urban Beauty Based on the 15 Properties of Living Structure*, §§3.1, 4.1.
- **Scoring prompt / 评分指令:** Original GPT instructions supplied by Professor Bin Jiang, reproduced in [SKILL.md](SKILL.md).
- **Terminology / 术语:** [十五项属性中英对照 / Bilingual glossary](references/rubric.md), including 强中心 (Strong Centers) and 厚边界 (Thick Boundaries). Terminology reference only; no additional scoring rubric.
- **Validation notes / 验证说明:** [EVALUATION.md](EVALUATION.md), separate from the scoring instructions.

The repository does not distribute the paper’s test images, GPT knowledge files, private conversations, or API credentials. / 仓库不分发论文测试图片、GPT 知识文件、私人对话或 API 凭据。
