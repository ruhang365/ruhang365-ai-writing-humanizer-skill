# Audit Contract

Use this when `ai-writing-humanizer` is part of an automated publishing workflow.

## Required JSON shape

```json
{
  "schema": "ruhang365.ai-writing-humanizer.audit.v1",
  "contentKey": "",
  "humanized": true,
  "sourceSkill": "ruhang365-ai-writing-humanizer",
  "skillVersion": "v3",
  "checkedAt": "",
  "inputContract": {
    "format": "",
    "authorIntent": "",
    "targetReader": "",
    "toneBoundary": "",
    "materialSource": ""
  },
  "detectedBuckets": [
    {
      "bucket": "material_gaps",
      "severity": "low|medium|high",
      "findings": []
    }
  ],
  "rewritesApplied": [],
  "preservedClaims": [],
  "factsNotInvented": true,
  "platformAdaptation": {
    "platforms": [],
    "notes": []
  },
  "finalAntiAiPass": {
    "residualIssues": [],
    "fixesApplied": [],
    "status": "passed"
  },
  "finalDecision": {
    "status": "passed",
    "publishable": true,
    "reason": ""
  }
}
```

## Compatibility

Existing workflows may also accept legacy records where `sourceSkill` contains `humanizer` and `finalDecision.status=passed`. New入行365社媒内容 should prefer `sourceSkill=ruhang365-ai-writing-humanizer`.

## Rules

- `factsNotInvented` must be `true` before publication.
- `finalDecision.publishable` must be `true` before publication.
- If important material is missing, either mark `publishable=false` or put the missing item in `suggestedAuthorAdditions`.
- Do not claim the skill was used unless the diagnostic and final anti-AI pass were actually performed.
