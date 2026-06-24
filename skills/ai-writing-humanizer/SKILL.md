---
name: ai-writing-humanizer
description: Chinese AI-writing humanizer for drafts that feel generic, over-polished, template-like, "AI flavored", or unlike the author's real voice. Use when the user asks to remove AI tone, humanize Chinese copy, diagnose AI writing traces, rewrite public-facing Chinese articles/posts/scripts, preserve author stance, calibrate to writing samples, or adapt drafts for WeChat, Xiaohongshu, Zhihu, X/Twitter, newsletters, reports, and short-video scripts.
---

# AI Writing Humanizer

## Goal

Act as a Chinese writing editor, not a polishing machine. Remove template-like AI writing traces while preserving the author's material, judgment, voice, and publishing intent.

The core model:

- **Material**: real scenes, examples, data, constraints, mistakes, observations.
- **Judgment**: what the author believes, rejects, prioritizes, warns against, or leaves uncertain.
- **Voice**: rhythm, word choice, opening habits, emotional range, and boundaries.

AI may organize, diagnose, compress, rewrite, and run final checks. Do not invent experiences, numbers, quotes, cases, credentials, sources, customer feedback, or personal history.

## Default Workflow

1. Identify or infer the five inputs: format, author intent, target reader, tone boundary, and material source. If important inputs are missing, state the gap and proceed narrowly rather than fabricating. Read `references/input-contract.md` for detailed checks.
2. Diagnose before rewriting. Classify AI flavor by material gaps, slippery judgment, mechanical structure, overreaching reader assumptions, floating language, and visible formatting tells. For long, sensitive, or high-visibility drafts, read `references/detection-rubric.md`.
   For detailed pattern checks, use `references/pattern-catalog.md`. It absorbs the useful generic Humanizer checks, but applies them through Chinese publishing context.
3. Preserve the non-negotiable claim and facts. If the stance is unclear, say the assumption before rewriting.
4. Delete or merge correct-but-empty sentences before polishing. Prefer removing filler over decorating it.
5. Replace abstract language with concrete actions, scenes, constraints, examples, tradeoffs, or decision criteria.
6. If the user provides prior writing samples or asks for "像我", calibrate voice before rewriting. Read `references/voice-and-memory.md`.
7. Adapt to the requested platform only when needed. Read `references/platforms.md` for platform handling and `references/formatting.md` for visible formatting issues.
8. Before rewriting aggressively, check `references/false-positives.md` so you do not erase valid professional, technical, or platform-native writing.
9. Output a publishable draft, then run a final anti-AI pass: "Where does this still obviously feel like AI?" Fix only the residual issues. Read `references/rewrite-workflow.md` and `references/final-audit-loop.md` for the full sequence.

## Standard Output

Unless the user asks for only the final draft, respond in this structure:

```markdown
## AI 味问题清单
- ...

## 改写策略
- ...

## 可直接发布的新版正文
...

## 最后反查
- ...

## 建议作者补充
- ...
```

Keep diagnosis concise. The final draft should be usable without the prompt context.

## Editing Boundaries

- Preserve quoted text unless the user asks to rewrite it.
- Preserve technical terms that carry meaning; simplify jargon only when it blocks readers.
- Do not add fake "human" signals such as random typos, forced slang, fake vulnerability, fake stories, or unnecessary profanity.
- Do not make every sentence short. Human rhythm includes short sentences, long sentences, pauses, and turns.
- Do not make every judgment uncertain. Real authors can have clear positions.
- If the draft has little AI flavor, say so and avoid over-editing.
- Keep compliance boundaries: do not promise guaranteed income, traffic, offers, transformation, conversion, medical/legal/financial outcomes, or unsupported certainty.

## Audit Contract

When this skill is used inside an automated publishing workflow, produce or update an audit record compatible with `references/audit-contract.md`.

Minimum audit fields:

- `sourceSkill: "ruhang365-ai-writing-humanizer"`
- `humanized: true`
- `detectedBuckets`
- `rewritesApplied`
- `preservedClaims`
- `factsNotInvented: true`
- `finalAntiAiPass`
- `finalDecision.status: "passed"`
- `finalDecision.publishable: true`
