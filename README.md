# skill-adr: Agent skill for working with a lightweight ADR documentation

An Agent Skill for creating, updating, and reviewing Markdown Architecture
Decision Record (ADR) documentation projects. This skill is intentionally dedicated for working with simplified version of ADR that we find most useful for the majority of the projects:

- Context
- Decision
- Consequences
- Alterntives cosidered

This skill is also intentionally tool-agnostic. It follows the portable
[Agent Skills](https://skill.md/) format and does not require Codex, OpenAI or any ADR-specific generator.

## Layout

```text
skill-adr/
|-- README.md
`-- SKILL.md
```

`SKILL.md` is the skill package. It contains the required `name` and
`description` frontmatter plus the instructions an agent should follow.

## Install

Copy or clone this directory into any Agent Skills-compatible client.

For tools that load skills from a local skills directory, keep the folder name
as `skill-adr` because the skill name in `SKILL.md` matches the parent
directory.

## Validate

Validate with the reference Agent Skills validator:

```bash
skills-ref validate /path/to/skill-adr
```

If `skills-ref` is not installed, install it from the Agent Skills reference
implementation:

```bash
python3 -m venv /tmp/skills-ref-venv
. /tmp/skills-ref-venv/bin/activate
pip install 'git+https://github.com/agentskills/agentskills.git#subdirectory=skills-ref'
skills-ref validate /path/to/skill-adr
```
