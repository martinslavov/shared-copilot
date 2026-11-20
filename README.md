# Shared Copilot

A shared repository for Copilot agents, skills, and related instructions and resources. Its purpose is to maintain these components in one place and make them reusable across projects.

## Contents

- **Agents** — specialized roles with a defined area of responsibility and workflow.
- **Skills** — reusable instructions and supporting materials for specific tasks.
- **Related resources** — shared instructions, templates, examples, and configuration used by agents and skills.
- **Prompt evaluation criteria** — definitions and scoring guidance in [`docs/prompt-evaluation-criteria.md`](docs/prompt-evaluation-criteria.md).

## Organization

Components are grouped by type to make them easy to discover and use. For example:

```text
.
├── agents/       # Agent definitions
├── skills/       # Skill definitions and their resources
├── instructions/ # Shared instructions
└── templates/    # Templates and examples
```

The structure can grow as needed. Each component should include the files it requires and clear usage instructions.

## Adding a component

1. Place the agent, skill, or resource in the appropriate directory.
2. Give it a descriptive name and state its purpose clearly.
3. Document how to use it, its inputs, and the expected result.
4. Keep shared instructions in one place instead of duplicating them across components.

## Maintenance

Changes to this repository may affect more than one project. Keep components self-contained, consistent with shared instructions, and up to date with how they are used.
