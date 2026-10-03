# Beautimeter Research Skill / Beautimeter 研究版 Skill

**两张图片，两个分数。用活力结构十五项属性，探索图像中的美。**

**Two images, two scores. Explore beauty through the fifteen properties of living structure.**

[中文](#中文) · [English](#english) · [评分指令 / Scoring instructions](SKILL.md)

## 中文

Beautimeter Skill 让支持图片理解的 AI 比较两张图，并分别给出 **0–15 分**的美度评分，默认不展开解释。

它依据 **Bin Jiang 教授的 Beautimeter 论文和教授提供的原始 GPT 指令**整理，使用 Christopher Alexander 的活力结构十五项属性，每项计 0–1 分。你可以选择所用的图片理解模型，无需依赖原 Beautimeter GPT 的分享链接。

### 怎么用？

**直接试用，不需要安装：**

1. 打开 [SKILL.md](SKILL.md)，复制其中英文代码框里的原始评分指令。
2. 在支持图片理解的 AI 中新建对话，依次上传两张图片，再粘贴指令并发送。
3. 查看两个总分：图像 1 对应先上传的图片，图像 2 对应后上传的图片。

**在 Codex 中作为 skill 使用：**

安装到本地 skills 目录：

```powershell
git clone https://github.com/eleanor-wsyy/beautimeter-research-skill.git "$HOME/.codex/skills/beautimeter-skill"
```

安装后，在新对话中依次上传两张图片，输入：

```text
用 $beautimeter-skill 给这两张图打分，只显示两个总分。
```

### 使用前了解

这是可分享的研究版指令包，不是在线评分网站，也不是原 GPT 的导出副本。分数可能随模型、API 服务和对话上下文变化，适合作为比较与讨论的参考，不能视为已经验证的客观美度测量。更多说明见 [验证说明](EVALUATION.md)。

## English

Beautimeter Skill asks a vision-capable AI to compare two images and give each a **score from 0 to 15**, with no explanation by default.

It is based on **Professor Bin Jiang’s Beautimeter paper and the original GPT instructions he shared**. It uses Christopher Alexander’s fifteen properties of living structure, with each property scored from 0 to 1. You can choose your vision model without relying on the original Beautimeter GPT’s sharing link.

### How to use

**Try it without installing anything:**

1. Open [SKILL.md](SKILL.md) and copy the original scoring prompt from the English text block.
2. Start a new conversation in a vision-capable AI, attach two images in order, and send the prompt.
3. Read the two totals: Image 1 is the first attachment; Image 2 is the second.

**Use it as a skill in Codex:**

Install in your local skills directory:

```sh
git clone https://github.com/eleanor-wsyy/beautimeter-research-skill.git "$HOME/.codex/skills/beautimeter-skill"
```

Then attach two images in a new conversation and ask:

```text
Use $beautimeter-skill to score these two images; show only the two totals.
```

### Before you use it

This is a shareable research instruction package, not an online scoring website or an exported copy of the original GPT. Scores may vary with the model, API service, and conversation context. Use them to support comparison and discussion, not as a validated objective measure of beauty. See the [validation notes](EVALUATION.md) for more detail.

## 来源与参考 / Sources and references

- **方法 / Method:** Bin Jiang, *Beautimeter: Harnessing GPT for Assessing Architectural and Urban Beauty Based on the 15 Properties of Living Structure*, §§3.1, 4.1.
- **原始指令 / Original prompt:** 教授提供的 GPT 评分指令，保留在 [SKILL.md](SKILL.md)。 / The GPT scoring instructions shared by Professor Bin Jiang, preserved in [SKILL.md](SKILL.md).
- **术语 / Terminology:** [十五项属性中英对照 / Bilingual glossary](references/rubric.md)，包括强中心（Strong Centers）和厚边界（Thick Boundaries）。仅供术语查询，不增加评分规则。 / For terminology only, with no additional scoring rules.

仓库不包含 API 密钥，也不分发论文测试图片、GPT 知识文件或私人对话。

The repository contains no API keys and does not distribute the paper’s test images, GPT knowledge files, or private conversations.
