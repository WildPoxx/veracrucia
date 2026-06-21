# Claude Skills Index - Veracrucia

Este arquivo e o espelho visivel das skills do projeto. Se Claude nao enxergar `.claude/skills/`, use este indice como roteamento operacional.

## Ordem de leitura

1. `CLAUDE.md`
2. `AI_COLLABORATION.md`
3. `docs/project/VERACRUCIA_PUBLIC_BIBLE.md`
4. `docs/ai/PROJECT_KNOWLEDGE_COVERAGE.md`
5. `docs/ai/VERACRUCIA_PRIVATE_CONTEXT_PACKAGE.md`
6. Skill relevante para a tarefa

## Skills

### veracrucia-authorial-style

Arquivo:

```text
.claude/skills/veracrucia-authorial-style/SKILL.md
```

Use para escrita, reescrita, revisao de voz, calibracao de estilo, anti-AI pass, prosa de cena e fidelidade a linguagem autoral de Mario em Veracrucia.

### veracrucia-scene-planner

Arquivo:

```text
.claude/skills/veracrucia-scene-planner/SKILL.md
```

Use para planejar cenas antes da redacao: identidade da cena, funcao dramatica, POV, eventos obrigatorios, materialidade, virada, promessa, progresso e payoff.

### veracrucia-editorial-diagnostics

Arquivo:

```text
.claude/skills/veracrucia-editorial-diagnostics/SKILL.md
```

Use para parecer critico, diagnostico de cena/capitulo, avaliacao de qualidade literaria, continuidade, problemas de POV, estrutura, ritmo e plano editorial.

### veracrucia-reference-decoupage

Arquivo:

```text
.claude/skills/veracrucia-reference-decoupage/SKILL.md
```

Use para analisar autores, romances, contos ou trechos de referencia como mecanismos formais, com adaptacao para Veracrucia e alerta contra imitacao.

## Combinacoes frequentes

- Planejar cena e depois escrever: `veracrucia-scene-planner` primeiro, `veracrucia-authorial-style` depois.
- Avaliar uma cena ja escrita: `veracrucia-editorial-diagnostics`; se o problema for voz ou prosa, combinar com `veracrucia-authorial-style`.
- Estudar um autor para incorporar tecnica: `veracrucia-reference-decoupage`; so depois converter em regra de cena ou estilo.
