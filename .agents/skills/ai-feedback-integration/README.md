# ai-feedback-integration

`ai-feedback-integration` is an instruction-only AI skill that appends a post-execution feedback loop to another skill.

Example use:

```text
Create a skill called x that does a, b and c, /ai-feedback-integration
```

The skill tells the AI to add a final section to the target skill that:

- asks the user whether they want to suggest improvements, but only after the target skill has completed its normal output;
- collects feedback if the user says yes;
- proposes a specific skill/process improvement;
- asks for approval before making any change; and
- incorporates the approved change into the target skill where possible.

## Contents

- `SKILL.md` — the skill instructions and metadata.
