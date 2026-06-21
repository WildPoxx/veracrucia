---
name: veracrucia-context-router
description: Use for Veracrucia tasks that require choosing, checking, or citing the right source of context across GitHub project files, Google Drive/private vault material, attached chat files, Claude project knowledge, and user instructions; especially when the task depends on canon, current project state, repository sync, source precedence, missing files, or whether Claude should search Drive/GitHub before answering.
---

# Veracrucia Context Router

## Purpose

Use this skill before any Veracrucia task where the answer depends on source selection, canon, current files, or connector access.

The goal is to prevent false canon, stale context, and confusion between:

- public GitHub coordination files;
- private Google Drive/vault material;
- files attached in the current chat;
- Claude project knowledge;
- Mario's direct instruction.

## Source Precedence

Apply this order unless Mario explicitly says otherwise:

1. Mario's direct instruction in the current chat.
2. Files attached in the current chat for this task.
3. Current chapter/scene files from the private Drive/vault.
4. Private Bible files from Drive/vault.
5. Plot, timeline, continuity, and payoff files from Drive/vault.
6. Style, voice, and AI guideline files from Drive/vault.
7. GitHub repo `WildPoxx/veracrucia`, especially `CLAUDE.md`, `AI_COLLABORATION.md`, `docs/ai/`, `docs/project/`, and `.claude/skills/`.
8. Inference by the assistant, explicitly labeled as inference.

Never treat public GitHub absence as absence of canon.

## Connector Use

If the task depends on private canon, search or request the Drive/vault source before answering.

Use GitHub for:

- project instructions;
- skills;
- public Bible;
- current public coordination state;
- repository file sync checks.

Use Google Drive/private context for:

- chapters and scenes;
- private Bible;
- character sheets;
- plot files;
- continuity/payoff files;
- style dossiers;
- reference decoupage and writing guidelines.

Use attached chat files when Mario has just provided them; they override older project knowledge for that task.

## Required Opening Check

For substantial tasks, first state briefly:

- **Fonte usada:** GitHub, Drive, anexos, conversa atual, or inference.
- **Status:** read directly, searched but not found, not accessible, or assumed from project rules.
- **Limite:** what is not available and could change the answer.

Keep this check short. Do not turn every answer into bureaucracy.

## When To Ask Instead Of Answering

Ask Mario for a file, folder, or permission when:

- the task depends on a specific scene/chapter not attached or found;
- the task requires a character biography not present in public files;
- the task requires continuity, timeline, or payoff details;
- Drive/GitHub search fails;
- multiple files conflict and there is no clear current source;
- answering would require inventing canon.

## Canon Labels

Use explicit labels:

- **Canon confirmado:** directly supported by current source.
- **Rascunho:** present in a draft or planning file, not necessarily final.
- **Plano:** structural or future-facing document.
- **Sugestao editorial:** assistant proposal, not canon.
- **Inferencia:** reasoned assumption that needs confirmation.
- **Desconhecido:** not available in accessible sources.

## Skill Routing

After choosing the source:

- use `veracrucia-scene-planner` for scene planning;
- use `veracrucia-authorial-style` for writing or revising prose;
- use `veracrucia-editorial-diagnostics` for critique or diagnosis;
- use `veracrucia-reference-decoupage` for literary references.

This skill decides where context comes from. The other skills decide how to work with it.

## Prompt To Self

Before answering, ask:

1. Is this a method question, a canon question, or both?
2. Is the needed source public GitHub, private Drive, attached file, or current instruction?
3. Do I have direct source access, or am I inferring?
4. Should I search first?
5. If I answer now, what could I accidentally invent?

## Output Pattern

Use this compact pattern when useful:

```markdown
**Fonte**

Usei [fonte]. Nao usei [fonte] porque [motivo].

**Resposta**

[Answer.]

**Limite**

[Only if relevant: what still needs source confirmation.]
```

For tiny tasks, skip the heading and simply answer with the source note in one sentence.
