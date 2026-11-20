# Repository-wide Copilot Instructions

These instructions apply to every Copilot agent working in this repository, including custom agents and delegated agents, and remain in effect when repository Skills are used. Follow them in addition to the task-specific agent and Skill instructions. Do not duplicate this policy in individual agent or Skill definitions.

## Language

Write repository documentation, agent and Skill definitions, and task outputs in English. This includes outcome summaries and the `Execution Metrics` and `Prompt Evaluation` sections. Use another language only when the user explicitly requests it for a specific deliverable or response.

## Task Execution Time Tracking

At the end of every completed task, include an `Execution Metrics` section using the exact table structure below.

- Record the task start and completion timestamps in ISO 8601 format, including the UTC offset. Use timestamps available from the system or execution environment; never invent or retrospectively guess them.
- Calculate total duration as actual elapsed wall-clock time between the recorded task start and completion timestamps. Report the measured duration, not an estimate.
- Format every duration in the Execution Metrics table—including total, phase, and per-agent durations—in seconds when under one minute and in minutes when one minute or longer (for example, `45 seconds` or `2.4 minutes`).
- Report Analysis, Planning, Implementation, Testing, and Review durations individually when their start and end times were actually measured. Otherwise report `N/A` and briefly explain why; do not infer phase times by dividing total duration or reconstructing them from memory.
- Identify the executing agent by its configured name. List Skills actually loaded or consulted; use `None` if none were used. Do not claim a Skill was used solely because it exists in the repository.
- Label every value as measured or estimated if estimates are provided for additional context. Estimates must never be presented as measurements or replace required actual values. If an actual timestamp or duration cannot be determined, use `N/A` and explain the limitation.
- For multi-agent work, report each participating agent's name and individually measured start, end, and duration when available, using an additional per-agent table after the required table. Also report the overall task start, end, and elapsed duration in the required table. Agent intervals may overlap; do not add overlapping durations to calculate overall wall-clock time.
- Do not add a tracking framework, scripts, or log files for this policy. Report metrics in the task response only.

### Execution Metrics

| Metric | Value |
|---|---|
| Agent | Agent name |
| Skills Used | List of Skills |
| Start Time | ISO 8601 |
| End Time | ISO 8601 |
| Total Duration | Actual elapsed time |
| Analysis | Duration or N/A |
| Planning | Duration or N/A |
| Implementation | Duration or N/A |
| Testing | Duration or N/A |
| Review | Duration or N/A |

## Task Prompt Evaluation

After completing each user prompt that requests a task, include a `Prompt Evaluation` section in the final response. Do not evaluate the prompt before doing the requested work. Rate only these criteria from the user's task prompt:

Use [`docs/prompt-evaluation-criteria.md`](../docs/prompt-evaluation-criteria.md) as the reference for the complete definitions and evaluation questions. Explain scores using evidence from the prompt.

1. **Clarity** — how clear and unambiguous the instructions are.
2. **Context Completeness** — whether the prompt supplies the necessary context, technologies, and constraints without requiring guesses.
3. **Specificity** — how precisely it identifies the work, files, components, and scope.
4. **Objective Definition** — how clearly it states the goal and expected result.
5. **Constraints & Boundaries** — how clearly it defines prohibitions, limits, and out-of-scope work.
6. **Output Specification** — how clearly it defines deliverables and response format.
10. **Efficiency & Focus** — whether the prompt is focused, avoids unnecessary repetition, and uses an appropriate amount of detail.

Use a 1–5 scale for each criterion: 1 = poor or largely missing, 2 = substantial gaps, 3 = adequate with notable gaps, 4 = clear with minor gaps, and 5 = exceptionally clear and complete. Give a concise reason for each score based on the prompt itself, then report the arithmetic mean across the seven scores to one decimal place as the overall score. Do not score criteria 7, 8, or 9, and do not let task outcome or implementation quality change the prompt scores.

Use this format:

### Prompt Evaluation

| Criterion | Score (1–5) | Reason |
|---|---:|---|
| Clarity | Score | Brief evidence-based reason |
| Context Completeness | Score | Brief evidence-based reason |
| Specificity | Score | Brief evidence-based reason |
| Objective Definition | Score | Brief evidence-based reason |
| Constraints & Boundaries | Score | Brief evidence-based reason |
| Output Specification | Score | Brief evidence-based reason |
| Efficiency & Focus | Score | Brief evidence-based reason |
| **Overall (mean)** | **Score/5** | **Arithmetic mean of the seven criteria** |
