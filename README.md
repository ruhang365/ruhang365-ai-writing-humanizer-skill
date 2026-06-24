# 入行365去 AI 味写作 Skill v2

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

这是入行365原创的中文写作 Skill，用来把一篇看起来完整但很像 AI 写的初稿，改成更有材料、判断、作者声音和发布价值的内容。

它不是“润色提示词”。v2 的重点是：

- 先判断 AI 味来自哪里：材料空、判断滑、结构机械、站位越位、语言漂浮，还是格式露馅。
- 先删掉正确但没信息量的水分，再做改写。
- 保留作者原本的立场和声音，不把所有人都改成同一种“通用人类腔”。
- 做最后反查，专门找改完以后残留的 AI 味。

完整方法说明见入行之路文章：

https://rhzl.ruhang365.cn/articles/ai-writing-humanizer-skill

## 适合谁

- 正在用 AI 写公众号、小红书、知乎、X、视频脚本的内容创作者。
- 帮客户交付文章、脚本、方案的 AI 服务者。
- 想把自己的经验整理成方法论，但不想被 AI 磨平成模板的人。

## 30 秒复制版

把下面这段复制给你正在使用的 AI，然后贴上你的初稿：

```markdown
你是我的中文写作编辑。你的目标不是把文章改得更顺，而是保留真实材料、作者判断和个人声音，去掉模板化 AI 写作痕迹。

处理前先确认 5 项：体裁、作者意图、目标读者、语气边界、素材来源。信息不足时，先说明缺口，宁可写窄一点，不要自动编故事、数据、案例或来源。

请按这个流程处理：
1. 先输出 AI 味检测报告，不要直接改。
2. 按材料空、判断滑、结构机械、站位越位、语言漂浮、格式露馅分类列出问题。
3. 标出正确但没有信息量的句子，并建议删除或合并。
4. 保留核心观点，把抽象表达改成具体动作、场景、限制或判断标准。
5. 如果我提供了过往样稿，先做声音校准：学习我的句长、开头方式、常用词、语气边界，不要把我改成另一种通用人类腔。
6. 输出可直接发布的新版正文。
7. 最后做一次反查：指出新版哪里还像 AI，并给出最终修订版。

边界：不编造个人经历、数字、引语、案例、身份、客户反馈和外部来源。整体没有明显 AI 味时，不要为了修改而修改。
```

## ChatGPT / Claude / Cursor 用法

如果你不使用 Codex Skill，直接复制上面的 30 秒版本即可。建议补一句任务目标：

```text
请把下面这篇初稿改成公众号文章开头。目标读者是刚开始用 AI 写内容的运营和自媒体人。保留我的核心观点，不要编造经历。
```

如果你长期使用 Cursor、Claude Code 或其他 Agent，可以把 `skills/ai-writing-humanizer/SKILL.md` 保存成项目写作规则，再按需引用 `references/` 里的检测和改写清单。

## Codex / OpenAI Skill 用法

仓库里包含标准 Skill 目录：

```text
skills/ai-writing-humanizer/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── detection-rubric.md
    ├── formatting.md
    ├── input-contract.md
    ├── platforms.md
    ├── rewrite-workflow.md
    └── voice-and-memory.md
```

安装到本机 Codex：

```bash
git clone https://github.com/ruhang365/ruhang365-ai-writing-humanizer-skill.git
cd ruhang365-ai-writing-humanizer-skill
mkdir -p ~/.codex/skills
cp -R skills/ai-writing-humanizer ~/.codex/skills/
```

安装后，新开一个 Codex 对话或重启 Codex，让 Skill 元数据重新加载。

使用时可以直接说：

```text
Use $ai-writing-humanizer 帮我把下面这篇小红书初稿去 AI 味，保留我的观点，但改得更像真实创作者写的。
```

## 示例

- `examples/basic-rewrite.md`：典型 AI 味初稿的诊断和改写。
- `examples/voice-calibration.md`：用户要求“像我”时如何先做声音校准。

## 授权

本文档、提示词、示例和 Skill 内容采用 `CC BY 4.0` 授权。你可以复制、改编、用于自己的工作流，但请保留来源署名：

> 入行365 / 煜建未来：去 AI 味写作 Skill
>
> https://github.com/ruhang365/ruhang365-ai-writing-humanizer-skill

如果后续加入脚本或程序代码，代码部分会单独标注开源许可证。
