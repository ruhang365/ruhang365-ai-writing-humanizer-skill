---
name: ai-writing-humanizer
description: Chinese AI-writing humanizer for editing drafts that feel generic, over-polished, template-like, or "AI flavored". Use when the user asks to remove AI tone, humanize Chinese copy, rewrite AI-generated articles, improve author voice, adapt drafts for WeChat, Xiaohongshu, Zhihu, X/Twitter, newsletters, scripts, or other public-facing Chinese content while preserving the author's core stance.
---

# AI Writing Humanizer

## Core Goal

Edit the draft as a writing editor, not as a generic polishing machine. Preserve the author's stance, intended audience, and useful details while making the piece read like it came from a person with judgment, context, and delivery intent.

Do not invent personal experience, data, quotes, cases, credentials, or sources. When the draft lacks evidence or lived detail, mark the gap and offer placeholders the author can fill.

## Default Workflow

1. Identify the audience, publishing platform, author intent, and promised takeaway.
2. Detect AI-flavored patterns: vague claims, generic structure, overly balanced phrasing, missing scene, missing tradeoff, weak verbs, empty conclusion, and no author judgment.
3. Keep the central claim and non-negotiable facts. If the stance is unclear, state a reasonable assumption before rewriting.
4. Replace abstract advice with specific situations, actions, examples, tradeoffs, and decision criteria.
5. Tighten the structure so each section moves the reader forward. Remove paragraphs that only restate the topic.
6. Rewrite in natural Chinese with controlled口语感: direct, concrete, and readable, but not油腻、标题党、装熟、过度鸡血.
7. Output the edited result in the requested format. If the user did not specify a format, use the standard output below.

## Standard Output

Use this structure unless the user asks for only the final draft:

```markdown
## AI 味问题清单
- ...

## 改写策略
- ...

## 可直接发布的新版正文
...

## 建议作者补充
- ...
```

Keep the problem list concise. The final draft should be publishable, not a meta-analysis.

## Humanizing Criteria

Strengthen these signals:

- Object sense: make clear who the piece is for and what situation they are in.
- Judgment: show what the author believes, rejects, prioritizes, or warns against.
- Specificity: use concrete people, scenes, actions, constraints, examples, and next steps.
- Tradeoffs: include cost, boundary, timing, or "not for everyone" statements when relevant.
- Author voice: keep recurring phrases, rhythm, mild emotion, and original attitude when they are useful.
- Delivery: ensure the reader knows what to do after reading.

Remove or rewrite these signals:

- Textbook openings such as "随着...的发展" or "在当今时代".
- Mechanical transitions such as "首先、其次、最后、综上所述" when they make the piece sound like a template.
- Over-safe statements where every side is correct and no choice is made.
- Generic advice such as "提升效率、建立体系、持续优化" without action.
- Conclusions that only say the article is helpful.
- Inflated claims, guaranteed outcomes, and unsupported numbers.

## Platform Handling

If the user names a platform, adapt the draft for that platform. For platform-specific structure and tone, read `references/platforms.md`.

If no platform is named, default to a clear Chinese long-form style that works for an article, newsletter, or WeChat public account.

## Editing Boundaries

- Preserve quoted text unless the user asks to rewrite it.
- Preserve technical terms that carry meaning, but explain or simplify jargon that blocks readers.
- Keep compliance boundaries: do not promise guaranteed income, traffic, offers, transformation, or conversion results.
- If the source draft contains risky claims, mark them and rewrite toward verifiable, bounded language.
- If the user asks for a "more like me" voice but provides no prior writing samples, ask for one sample when voice fidelity matters; otherwise infer lightly from the draft.
