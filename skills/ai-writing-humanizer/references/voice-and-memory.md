# Voice And Memory

Use this when the user asks for "像我", "保留我的口气", "个人 IP 文风", or provides prior writing samples.

## Voice Calibration

Before rewriting, inspect 2-3 supplied samples for:

- Sentence length: mostly short, mixed, or long with pauses.
- Opening habit: direct judgment, scene, question, contrast, or context setup.
- Common phrases: words the author naturally repeats.
- Emotional range: calm, sharp, playful, restrained, irritated, reflective.
- Transition style: abrupt turns, numbered logic, story-to-lesson, or direct conclusion.
- Forbidden upgrades: words that would sound more polished but less like the author.

Then state the calibration briefly before rewriting.

## Do Not Overfit

- Do not copy private details from samples into the new draft unless the user asks.
- Do not imitate typos, filler, or weak habits unless they are intentional style.
- Do not make every sentence match the sample length. Preserve rhythm, not surface quirks.
- Do not turn "humanized" into fake slang or fake vulnerability.

## Long-Term Author Profile

For repeated use, suggest a compact author profile with:

- Who the author is and what they write about.
- Reader groups and common reader stuck points.
- Preferred tone and forbidden tone.
- Recurring judgments and boundaries.
- Allowed source material and forbidden invented material.
- Workflow preference: ask first, diagnose first, rewrite directly, or produce variants.

For coding agents, this profile can live in `AGENTS.md` or `CLAUDE.md`. For chat products, it can live in custom instructions or memory. These stores do not automatically sync.
