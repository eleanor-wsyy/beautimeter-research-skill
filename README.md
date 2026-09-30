# Beautimeter Research Skill / Beautimeter 研究版 Skill

**中文** · 这是根据 Bin Jiang 的 Beautimeter 论文独立编写的研究原型，**不是教授原有 GPT 的导出版本、官方工具或已校准的替代品**。仓库不包含教授的私有指令、知识文件、测试图像或 API 密钥。

**English** · This is an independent, paper-guided research prototype, **not an export of Professor Bin Jiang’s original GPT, an official tool, or a calibrated replacement**. The repository contains none of the professor’s private instructions, knowledge files, test images, or API keys.

[中文说明](#中文说明) · [English guide](#english-guide)

## 中文说明

### 它做什么

输入**两张图片**，按 Christopher Alexander 的活力结构十五项属性进行初步比较。Skill 保留图片顺序，先观察多尺度中心及其相互支撑关系，再记录逐项可见依据与暂定分数。看不到的结构可标为 `N/A`，不会当作零分；有缺项时不提供貌似完整的 `/15` 总分。

十五项中英文名称与 Studio 的 *Properties* 词表一致；完整译名和判读问题见 [`references/rubric.md`](references/rubric.md)。分数是对**所给图像中可见结构**的解释，不等于建筑整体的客观美度，也不代表教授 GPT 的输出。

### 安装和使用

此仓库目前为**私有**，克隆者须拥有访问权限。将仓库放在 Codex 的用户级 skills 目录，文件夹名保持 `beautimeter-skill`：

```powershell
git clone https://github.com/eleanor-wsyy/beautimeter-research-skill.git "$HOME/.codex/skills/beautimeter-skill"
```

如果设置了 `CODEX_HOME`，请改放到其中的 `skills/beautimeter-skill`。在新的 Codex 对话中上传两张图片，输入：

> 用 `$beautimeter-skill` 比较这两张图片；请展开十五项依据。

本 skill 不调用本项目的银河智算 API，但实际分析仍需宿主环境具备图像理解能力。**公开传播或以教授名义发布前，应先取得授权并用教授认可的新图对验证。**

## English guide

### What it does

Provide **two images** for a provisional comparison through Christopher Alexander’s fifteen properties of living structure. The skill preserves image order, reads the hierarchy of mutually supporting centers first, then records visible evidence and an indicative score for each property. Unobservable properties may be `N/A`, not zero; an incomplete assessment is not presented as a full `/15` total.

The English and Chinese property names match the Studio *Properties* catalog. See [`references/rubric.md`](references/rubric.md) for the complete bilingual list and evidence questions. Scores interpret **visible structure in the supplied photographs**, not the objective beauty of an entire building or the output of the professor’s GPT.

### Install and use

This repository is currently **private**; cloning requires access. Place it in your Codex user skills directory under the folder name `beautimeter-skill`:

```sh
git clone https://github.com/eleanor-wsyy/beautimeter-research-skill.git "$HOME/.codex/skills/beautimeter-skill"
```

If you use a custom `CODEX_HOME`, place it under that directory’s `skills/beautimeter-skill` instead. In a new Codex conversation, attach two images and ask:

> Use `$beautimeter-skill` to compare these two images and show the fifteen-property evidence table.

This skill does not use the project’s Galaxy AI API key, but a vision-capable host model is still required. **Obtain permission and validate on new professor-approved pairs before public distribution or any claim of official endorsement.**

### Source / 来源

Bin Jiang, *Beautimeter: Harnessing GPT for Assessing Architectural and Urban Beauty Based on the 15 Properties of Living Structure*. The skill paraphrases the paper’s task and theory of centers; its numeric interpretation remains provisional. See [`SKILL.md`](SKILL.md) for the operational instructions.
