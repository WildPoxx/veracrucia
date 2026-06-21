---
name: veracrucia-context-router
description: Use for Veracrucia tasks that require choosing, checking, or citing the right source of context across local workspace C:\Users\amari\source\Veracrucia, GitHub project files, Google Drive/private vault material, attached chat files, Claude project knowledge, and user instructions; especially when the task depends on canon, current project state, repository sync, source precedence, missing files, local filesystem access, or whether Claude should search Drive/GitHub/local files before answering.
---

# Veracrucia Context Router

## Purpose

Use this skill before any Veracrucia task where the answer depends on source selection, canon, current files, or connector access.

The goal is to prevent false canon, stale context, and confusion between:

- local Windows workspace: `C:\Users\amari\source\Veracrucia`;
- public GitHub coordination files;
- private Google Drive/vault material;
- files attached in the current chat;
- Claude project knowledge;
- Mario's direct instruction.

## Source Precedence

Apply this order unless Mario explicitly says otherwise:

1. Mario's direct instruction in the current chat.
2. Files attached in the current chat for this task.
3. Local workspace files in `C:\Users\amari\source\Veracrucia`, when the Claude surface has local filesystem access.
4. Current chapter/scene files from the private Drive/vault.
5. Private Bible files from Drive/vault.
6. Plot, timeline, continuity, and payoff files from Drive/vault.
7. Style, voice, and AI guideline files from Drive/vault.
8. GitHub repo `WildPoxx/veracrucia`, especially `CLAUDE.md`, `AI_COLLABORATION.md`, `docs/ai/`, `docs/project/`, and `.claude/skills/`.
9. Inference by the assistant, explicitly labeled as inference.

Never treat public GitHub absence as absence of canon.

## Local Workspace Access

Canonical local path on Mario's Windows machine:

```text
C:\Users\amari\source\Veracrucia
```

If running in Claude Code or another Claude surface with real local filesystem tools, actively search this path before answering canon-dependent questions.

Recommended local search order:

1. `03_CAPITULOS_E_CENAS/`, or the local accented folder with the same meaning, for current prose.
2. `01_BIBLIA/` for character, setting, institution, and system canon.
3. `02_ENREDOS_E_ESTRUTURAS/` for acts, plots, timelines, continuity, and payoffs.
4. `04_DIRETRIZES_IA/` for style, voice, decoupage, anti-AI, and writing rules.
5. `05_SUPORTE_DE_PROJETO/` for handoffs, operational context, and support files.
6. `06_REFERENCIAS/`, or the local accented folder with the same meaning, for reference inventory only when the task asks for references.

Use targeted search first: file names, character names, scene titles, chapter folders, terms like `GLIF`, `Axsoma`, `Eidolon`, `MotoZapp`, `Transcendencia`, `Continuidade`, `Payoff`.

Do not scan the whole vault for small tasks. If a broad search is needed, warn Mario and summarize the scope.

## Claude Surface Limitation

A skill cannot grant filesystem access by itself.

- In Claude web/project chat, use GitHub, Google Drive, project files, and attachments. If local `C:\...` is not accessible, say so and ask Mario to attach/sync the needed files or use Drive.
- In Claude Code/local sessions, use the local path directly.
- In Chrome-connected sessions, do not assume Chrome can read arbitrary local files unless Mario explicitly opens or attaches them.

## Connector Use

If the task depends on private canon, search or request the Drive/vault source before answering.

Use GitHub for:

- project instructions;
- skills;
- public Bible;
- current public coordination state;
- repository file sync checks.

Use local workspace or Google Drive/private context for:

- chapters and scenes;
- private Bible;
- character sheets;
- plot files;
- continuity/payoff files;
- style dossiers;
- reference decoupage and writing guidelines.

Prefer local workspace when available in a local Claude/Codex session. Prefer Google Drive when working in Claude web.

Use attached chat files when Mario has just provided them; they override older project knowledge for that task.

## Required Opening Check

For substantial tasks, first state briefly:

- **Fonte usada:** local workspace, GitHub, Drive, attached files, current chat, or inference.
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
2. Is the needed source local workspace, public GitHub, private Drive, attached file, or current instruction?
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
