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


### veracrucia-context-router

Arquivo:

```text
.claude/skills/veracrucia-context-router/SKILL.md
```

Use antes de tarefas que dependam de canon, busca de fonte, conectores, estado atual do projeto, arquivos anexados, workspace local `C:\Users\amari\source\Veracrucia`, GitHub, Google Drive, Project Knowledge ou conflito entre materiais. Esta skill decide de onde o contexto deve vir; as outras skills decidem como trabalhar com ele.

### veracrucia-repetition-control

Arquivo:

```text
.claude/skills/veracrucia-repetition-control/SKILL.md
```

Use para detectar e corrigir repeticoes literais, estruturas frasais recorrentes, movimentos retoricos repetidos, nomes reaproveitados, imagens/cadencias recorrentes e padroes estatisticos de LLM que parecem estilo mas enfraquecem a diferenca entre cenas, capitulos ou POVs.

## Combinacoes frequentes

- Sinopse prévia de capítulo antes da escrita: usar `veracrucia-context-router` para fonte e precedência, `veracrucia-scene-planner` para organizar função/cenas/PPP, `veracrucia-editorial-diagnostics` para ritmo/continuidade, `veracrucia-repetition-control` para padrões de repetição, e aplicar `docs/ai/REGRAS_DOS_4_4C_4E_4V.md`.
- Planejar cena e depois escrever: `veracrucia-scene-planner` primeiro, `veracrucia-authorial-style` depois.
- Avaliar uma cena ja escrita: `veracrucia-editorial-diagnostics`; se o problema for voz ou prosa, combinar com `veracrucia-authorial-style`.
- Estudar um autor para incorporar tecnica: `veracrucia-reference-decoupage`; so depois converter em regra de cena ou estilo.
- Qualquer tarefa com canon, workspace local, Drive, GitHub ou anexos: `veracrucia-context-router` primeiro, depois a skill especifica.
- Revisar cena com risco de repeticao de frase, estrutura, imagem, nome ou cadencia: combinar `veracrucia-authorial-style` ou `veracrucia-editorial-diagnostics` com `veracrucia-repetition-control`.

