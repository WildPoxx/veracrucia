---
name: veracrucia-repetition-control
description: Use for Veracrucia prose, scene revision, chapter diagnosis, or AI-assisted drafting when Claude or Codex must detect and prevent repeated phrases, repeated sentence structures, repeated rhetorical moves, repeated names, repeated images, or statistical LLM reuse across scenes, chapters, POVs, or different Mario Bastos projects.
---

# Veracrucia Repetition Control

## Purpose

Use this skill to catch false recurrence: patterns that look like style, motif, or thematic coherence but are actually model inertia, shortcut phrasing, or reused rhetorical machinery.

This skill complements `veracrucia-authorial-style` and `veracrucia-editorial-diagnostics`. It does not ban repetition. It asks whether repetition is deliberate, local, functional, and owned by Mario's project rather than by the model's statistical habits.

## Core Rule

Before accepting any expressive solution that feels polished, vivid, clever, aphoristic, or structurally neat, ask:

```text
Is this exact phrase, structure, image, name, rhythm, or argumentative move recurring because the work needs it, or because the model reached for a familiar pattern?
```

If the answer is uncertain, mark it as suspect and search or compare nearby project material before keeping it.

## Repetition Types

- **Literal repetition:** exact phrase, clause, image, punchline, title-like wording, or distinctive expression appears again.
- **Structural repetition:** same sentence architecture with different words, such as "X era A, B, C; personagem tinha D, E, F."
- **Functional repetition:** same narrative solution reused for different problems, such as institution-versus-affection, city-versus-body, body-versus-machine, or archive-versus-truth.
- **Rhetorical repetition:** neat antithesis, explanatory contrast, decorative triad, punchline paragraph, or "not merely X but Y" style move.
- **Imagetic repetition:** same family of sensory or symbolic images, such as metallic taste, dirty rain, concrete fatigue, city swallowing, body as machine, pressure in the ear.
- **Rhythmic repetition:** repeated cadence of short sentence clusters, setup-then-punchline, or isolated one-liners.
- **Onomastic repetition:** reused surnames, given names, brands, street names, institutions, acronyms, invented terms, or similar phonetic shapes.
- **POV leakage:** different focal characters using the same sentence habits, metaphors, joke structures, or conceptual grammar.

## Workflow

### 1. Identify Salient Material

Before revising or approving a passage, list mentally or explicitly:

- phrases that would be memorable if repeated;
- unusual metaphors;
- invented names or proper nouns;
- sentence structures with strong symmetry;
- enumerations or lists;
- one-line paragraphs;
- ideological or institutional formulations;
- sensory motifs.

Use this especially for AI-generated drafts and for passages Mario flags as "too familiar", "too polished", "too AI", "preguicoso", or "ja vi isso antes".

### 2. Test Function

For each salient item, ask:

- What information does it transmit?
- Does it arise from action, object, institution, body, route, weather, work, archive, or perception?
- Would the scene lose meaning if the shape changed?
- Is the same effect already carried by nearby action?
- Is this a motif Mario intentionally wants, or a default solution?

If the item mainly performs intelligence, theme, or profundity, rewrite from the information nucleus.

### 3. Search When Needed

For chapter or scene work in the local workspace, search before final judgment when a phrase or structure feels distinctive.

Use targeted searches such as:

```powershell
rg -n -i "key phrase|distinctive noun|proper name" 03_CAPITULOS_E_CENAS 02_ENREDOS_E_ESTRUTURAS 04_DIRETRIZES_IA
```

Search both exact words and functional neighbors. If a literal search fails but the pattern still feels repeated, trust the pattern diagnosis and mark it as structural repetition.

Do not scan the whole vault for every small line edit. Search when the item is salient, suspicious, or likely to recur across scenes.

### 4. Decide

Classify the recurrence:

- **Keep:** deliberate motif, clear POV ownership, or necessary continuity echo.
- **Vary:** useful information but repeated structure or wording.
- **Cut:** decorative, redundant, or explanatory recurrence.
- **Move to dossier/watchlist:** distinctive enough to track for the chapter or project.

## Watchlist Practice

For substantial chapter or scene revisions, maintain a short watchlist in the working answer or project notes when useful.

Use this shape:

```markdown
**Watchlist De Repeticao**

- Expressoes salientes:
- Estruturas salientes:
- Imagens salientes:
- Nomes proprios / termos inventados:
- Cadencias:
```

Examples of things to track:

- repeated institution-versus-affection contrast;
- repeated city-as-machine or body-as-machine metaphor;
- repeated dirty-rain/concrete/body sensory cluster;
- repeated invented name because it "sounds Veracrucia";
- repeated explanatory rhythm after concrete action already did the work.

Do not over-track neutral words. Track only items whose recurrence would be noticed or would flatten POV distinction.

## Repair Rules

- Replace repeated thesis-like structures with the concrete information the reader needs.
- Turn decorative lists into action, source, consequence, or perception.
- Keep at most one strong list unless another list performs a clearly different function.
- If a scene already shows the institution acting, avoid summarizing the institution as a concept.
- If one POV used a rhetorical move, do not give the same move to another POV unless the repetition is intentional.
- For names, search before inventing; prefer project-specific naming logic over model-default surnames or reused phonetics.
- For motifs, repeat by transformation, not copy: change context, object, pressure, and consequence.

## Output Guidance

When reporting a repetition issue, name the pattern, not only the sentence.

Good:

```text
This repeats the institutional/affective antithesis pattern: first a list of legal legitimacy, then a list of intimate traces. The scene already dramatizes the police barrier, so the sentence should return to the specific relationship.
```

Bad:

```text
This sounds repetitive.
```

When revising, preserve the information nucleus and change the mechanism.
