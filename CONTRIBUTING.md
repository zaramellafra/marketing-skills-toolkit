# Contributing to Marketing Skills

Thank you for your interest in contributing! This repository is a collection of marketing skills for AI agents (Claude, Gemini CLI, and ChatGPT). Every contribution helps marketers around the world work smarter.

---

## Before You Start

**Always open an issue before submitting a new skill or a significant change.**

This lets us discuss the idea, avoid duplicates, and make sure it fits the repository's direction before you invest time building it.

👉 [Open an issue](../../issues/new)

---

## What You Can Contribute

- **New skills** — a marketing framework or process not yet covered
- **Improvements to existing skills** — better workflows, additional references, new examples
- **Translations** — adapting a skill's output language or examples for a specific market
- **Bug fixes** — incorrect instructions, broken templates, or unclear copy

---

## Skill Structure

Every skill lives in its own folder under `skills/` and must follow this structure:

```
skills/
└── your-skill-name/
    ├── SKILL.md                  (required)
    ├── references/
    │   ├── frameworks.md         (optional — methodologies and theory)
    │   └── examples.md           (optional — real-world examples)
    ├── assets/
    │   └── output-template.md    (optional — ready-to-use output templates)
    └── evals/
        └── test-cases.md         (optional but encouraged for public skills)
```

---

## SKILL.md Format

Every `SKILL.md` must start with YAML frontmatter followed by the skill instructions in Markdown:

```markdown
---
name: your-skill-name
description: >
  Use this skill when [specific trigger]. Describe what the skill does
  and when an AI agent should activate it. Be specific — this is what
  determines when the skill gets used.
---

# Skill Title

Brief description of what this skill does.

## Language

Detect the user's preferred language from the `LANGUAGE` parameter or
from the first message. Respond entirely in that language.

## Workflow

### Step 1 — [Step name]

[Instructions]

### Step 2 — [Step name]

[Instructions]

## Output Template

[The structured output the AI should produce]

## Design Principles

[3–5 rules that define quality output for this skill]
```

---

## Naming Conventions

- Folder names: lowercase, hyphen-separated (`brand-positioning`, `email-nurture`)
- Be specific: `positioning` is better than `marketing-strategy`
- One framework or process per skill — don't bundle multiple methods into one

---

## Language & Tone

- All `SKILL.md` files and documentation are written in **English**
- Skills must support the `LANGUAGE` parameter so the AI responds in the user's language
- Keep instructions clear and direct — write for the AI agent, not for humans

---

## Step-by-Step Contribution Process

1. **Open an issue** describing the skill you want to add or the change you want to make
2. Wait for feedback — we'll confirm if it's a good fit and suggest any adjustments
3. **Fork the repository**
4. Create a new branch: `git checkout -b skill/your-skill-name`
5. Build your skill following the structure above
6. **Submit a Pull Request** referencing the original issue
7. We'll review, give feedback, and merge when it's ready

---

## Quality Checklist

Before submitting, make sure your skill:

- [ ] Has a `SKILL.md` with valid YAML frontmatter (`name` and `description`)
- [ ] Has a clear, specific `description` that explains when to trigger the skill
- [ ] Follows the workflow structure (numbered steps)
- [ ] Includes an output template
- [ ] Supports the `LANGUAGE` parameter
- [ ] Has at least 1 example in `references/examples.md` or `evals/test-cases.md`
- [ ] Uses a clear, hyphenated folder name

---

## Questions?

Open an issue with the `question` label and we'll get back to you.
