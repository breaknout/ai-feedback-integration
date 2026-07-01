---
name: ai-feedback-integration
description: Use when creating or updating another AI skill and the user wants a post-execution feedback loop added to that skill. Adds a governed improvement process that asks for user feedback only after the target skill runs, proposes a skill update, seeks approval, and then incorporates the approved change.
---

# AI Feedback Integration

## Purpose

This skill adds a reusable post-execution feedback and improvement process to the end of another skill being created or updated.

Use this skill when the user asks to create or revise a skill and explicitly invokes `ai-feedback-integration`, `/ai-feedback-integration`, or equivalent wording indicating that the target skill should include a post-run improvement loop.

## Core instruction

Add the following feedback-integration process to the end of the target skill being created or updated. It should appear as the final post-execution section of that skill, after the skill’s normal task-specific instructions, workflow, checks, and output requirements.

## Feedback-integration process to add to the target skill

After completing the skill’s normal output, ask the user:

> “Would you like to suggest any improvements to this skill based on how it performed in this run?”

Only ask this question after the skill has been fully executed. Do not ask it during setup, input collection, processing, or before delivering the skill’s main output.

If the user says no, end the interaction politely.

If the user says yes, ask them to describe the improvement they would like. Then analyse the feedback and propose a specific update to the skill. Present the proposed update clearly as a “Suggested Skill Improvement”, including:

1. the user’s feedback;
2. the process issue or opportunity identified;
3. the exact proposed change to the skill’s instructions, workflow, prompts, checks, or output format; and
4. why the change would improve future executions.

Do not update the skill immediately. Ask the user to approve the suggested improvement.

If the user approves the suggested improvement, incorporate the approved change into the skill’s instructions in the most appropriate location, preserving the existing structure and behaviour of the skill unless the approved improvement requires otherwise. Confirm that the skill has been updated and briefly summarise the change made.

If the user does not approve the suggested improvement, do not update the skill. Offer to revise the proposed improvement based on their further feedback.

## Integration rules

When adding this process to a target skill:

1. Place it at the very end of the target skill, under a clear heading such as `Post-execution feedback integration`.
2. Preserve the target skill’s existing purpose, workflow, constraints, tone, and output requirements unless the user has expressly asked to revise them.
3. Do not cause the target skill to ask for feedback before it has completed its normal task.
4. Do not make feedback collection mandatory.
5. Do not allow the target skill to self-modify without explicit user approval of a specific proposed change.
6. If the current environment can edit or update the target skill directly, apply the approved change there. If it cannot, provide the exact replacement text, patch, or revised `SKILL.md` section for the user to apply manually.
7. Keep the inserted process concise enough not to overwhelm the target skill, but complete enough to preserve the approval workflow.
