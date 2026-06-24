# 入行365去 AI 味写作 Skill

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

这是入行365原创的中文写作 Skill，用来把一篇看起来完整但很像 AI 写的初稿，改成更有判断、对象感、经验痕迹和发布价值的内容。

它不是“润色提示词”。它的重点是先找出内容为什么像 AI，再保留作者原本的判断，把空泛表达改成具体场景、真实动作和可交付的正文。

完整方法说明见入行之路文章：

https://rhzl.ruhang365.cn/articles/ai-writing-humanizer-skill

## 适合谁

- 正在用 AI 写公众号、小红书、知乎、X、视频脚本的内容创作者。
- 帮客户交付文章、脚本、方案的 AI 服务者。
- 想把自己的经验整理成方法论，但不想被 AI 磨平成模板的人。

## 30 秒复制版

把下面这段复制给你正在使用的 AI，然后贴上你的初稿：

```markdown
你是我的写作编辑，不是润色机器。你的目标不是把文章改得更顺，而是让文章更像一个有经验、有判断、有对象感的人写出来的。

请按以下步骤处理我给你的内容：

1. 判断目标读者是谁，他们现在真正关心什么。
2. 找出文章里的 AI 味：空泛表达、模板结构、过度正确、缺少场景、缺少个人判断、缺少具体动作。
3. 保留核心观点，不要擅自改变立场。
4. 把抽象表达改成具体场景，把泛泛建议改成可执行动作。
5. 保留适度口语感，但不要油腻、不要标题党、不要装熟。
6. 输出时分成三部分：
   - AI 味问题清单
   - 改写策略
   - 可直接发布的新版正文

写作风格要求：
- 像一个有实战经验的人在认真解释问题。
- 讲人话，但不要变成段子。
- 有判断，但不要武断。
- 有方法，但不要堆概念。
- 有个人口气，但不要自嗨。
```

## ChatGPT / Claude / Cursor 用法

如果你不使用 Codex Skill，直接复制上面的 30 秒版本即可。建议补一句任务目标：

```text
请把下面这篇初稿改成公众号文章开头。目标读者是刚开始用 AI 写内容的运营和自媒体人。保留我的核心观点，不要编造经历。
```

如果你在 Cursor 或 Claude Code 里长期使用，可以把 `skills/ai-writing-humanizer/SKILL.md` 的内容保存成自己的写作规则或项目内文档。

## Codex / OpenAI Skill 用法

仓库里已经包含标准 Skill 目录：

```text
skills/ai-writing-humanizer/
├── SKILL.md
├── agents/openai.yaml
└── references/platforms.md
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

看 `examples/basic-rewrite.md`，里面有一段典型 AI 味初稿、问题诊断、改写策略和完整改写结果。

## 授权

本文档、提示词、示例和 Skill 内容采用 `CC BY 4.0` 授权。你可以复制、改编、用于自己的工作流，但请保留来源署名：

> 入行365 / 煜建未来：去 AI 味写作 Skill
> https://github.com/ruhang365/ruhang365-ai-writing-humanizer-skill

如果后续加入脚本或程序代码，代码部分会单独标注开源许可证。
