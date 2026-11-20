# Prompt Evaluation Criteria

This document defines the criteria used to assess the quality of a user prompt. Use it as the reference when explaining what a criterion means or why a prompt received a particular score.

## 1. Clarity (Essential)

Measures how clear, specific, and understandable the instructions are.

- Are any instructions ambiguous?
- Are the instructions phrased concretely?
- Could the agent interpret the task in substantially different ways?

## 2. Context Completeness (Essential)

Measures whether the prompt provides the information needed to do the task without guessing.

- Is enough project or task context provided?
- Are relevant technologies and constraints identified?
- Is any important information missing that the agent would otherwise have to assume?

## 3. Specificity

Measures how precisely the prompt defines the work.

- Are there concrete instructions?
- Are files, components, or areas to change identified when relevant?
- Does the prompt avoid descriptions that are too broad?

## 4. Objective Definition

Measures how clearly the prompt states the intended goal and result.

- Is there a concrete end goal?
- Can the agent understand the problem to solve?
- Is the expected outcome defined?

## 5. Constraints & Boundaries

Measures how clearly the prompt defines limits and prohibited work.

- Does it prohibit unnecessary changes?
- Does it set relevant dependency, API, or architecture constraints?
- Does it identify work that is out of scope?

## 6. Output Specification

Measures how clearly the prompt defines the deliverables and response.

- Does it identify files to create or modify?
- Does it specify the expected response format?
- Does it say whether summaries, tests, or documentation are required?

## 7. Actionability

Measures whether the agent can proceed directly with the task.

- Is there enough information to begin?
- Are actions organized into logical steps when appropriate?
- Does the prompt provide actionable instructions rather than only general wishes?

## 8. Testability & Verification

Measures whether completion can be objectively verified.

- Are acceptance criteria provided?
- Are required tests or validation steps identified?
- Is it clear when the task is complete?

## 9. Consistency

Measures whether the requirements agree with one another and with applicable project guidance.

- Do any requirements contradict each other?
- Are the constraints compatible with the goal?
- Could the request conflict with engineering principles or other applicable skills?

## 10. Efficiency & Focus

Measures whether the prompt stays focused and uses an appropriate amount of detail.

- Is there unnecessary information?
- Are instructions repeated?
- Could the same result be achieved with less text without losing needed context?

## Scoring guidance

When a task requires a prompt evaluation, score only the criteria specified by the applicable repository instructions. For each scored criterion, use the following five-point scale and briefly justify the score with evidence from the prompt:

| Score | Meaning |
|---:|---|
| 1 | Poor or largely missing |
| 2 | Substantial gaps |
| 3 | Adequate, with notable gaps |
| 4 | Clear, with minor gaps |
| 5 | Exceptionally clear and complete |

If an overall score is requested, calculate the arithmetic mean of the included criterion scores and round it to one decimal place. Do not treat task implementation quality as evidence of prompt quality.
