# Example: Voice Calibration

## Task

The user asks: "保留我的口气，不要改得太像公众号模板。"

## What The Skill Should Do

Before rewriting, inspect supplied samples and report a compact calibration:

```markdown
## 声音校准
- 句子节奏：长短混合，常用短句停顿。
- 开头方式：通常先给判断，不先铺背景。
- 常用表达：偏直接，会用"这事真正麻烦的是..."这类转向。
- 语气边界：可以锋利，但不油腻、不鸡血。
- 禁止升级：不要把"这玩意儿"改成"该现象"，不要把判断改成咨询报告腔。
```

Then rewrite against that calibration. Do not copy facts from the sample unless the user explicitly says they are reusable.
