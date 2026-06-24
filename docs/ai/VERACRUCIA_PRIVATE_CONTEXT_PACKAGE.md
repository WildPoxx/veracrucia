# Veracrucia Private Context Package

Este documento define o pacote privado recomendado para dar ao Claude acesso canonico amplo sem publicar o corpus completo no GitHub.

O pacote em si deve ser fornecido por Project Knowledge privado, Google Drive conectado, upload manual ou outra fonte controlada por Mario. Este arquivo no GitHub publico e apenas o guia de montagem e leitura.

## Regra Central

O repositorio publico `WildPoxx/veracrucia` contem metodo, skills e uma Biblia Publica controlada. O canon detalhado vive no workspace privado local:

```text
C:\Users\amari\source\Veracrucia
```

Se Claude tiver acesso local ao Windows, deve usar `C:\Users\amari\source\Veracrucia` como raiz canonica local. Se estiver no Claude web, deve usar Google Drive, GitHub, Project Knowledge ou arquivos anexados, porque uma skill nao concede acesso direto ao disco C por si so. Em todos os casos, deve tratar os arquivos abaixo como fontes canonicas, respeitando a ordem de precedencia.

## Ordem De Precedencia

1. Instrucoes diretas de Mario na conversa atual.
2. Capitulos/cenas atuais em `03_CAPITULOS_E_CENAS/` ou na pasta local acentuada equivalente.
3. Biblia privada em `01_BIBLIA/`.
4. Estruturas de enredo e continuidade em `02_ENREDOS_E_ESTRUTURAS/`.
5. Diretrizes de estilo e IA em `04_DIRETRIZES_IA/`.
6. Skills e docs publicos do GitHub.
7. Inferencias do assistente, sempre marcadas como inferencias.

Handoffs recentes de Mario, Codex/local ou outra sessao autorizada contam como instrucoes diretas quando registram decisao posterior aos arquivos locais. Use-os para corrigir scaffolds antigos, mas nao publique no Git detalhes de manuscrito, estrutura fina de capitulos ou material sensivel.

## Pacote Minimo Recomendado

Para dar contexto forte sem carregar tudo, incluir:

- `01_BIBLIA/index_biblia.md`
- `01_BIBLIA/01_PERSONAGENS/00_index_personagens_geral.md`
- arquivo geral de Veracrucia em `01_BIBLIA/02_LOCAIS_E_CENARIO/America Lusitania/`
- arquivo principal de Sao Vicente em `01_BIBLIA/02_LOCAIS_E_CENARIO/Cidades/`
- `02_ENREDOS_E_ESTRUTURAS/03_ESTRUTURA_GERAL_DO_LIVRO/Matriz Critica dos 3 Atos.md` ou arquivo equivalente acentuado
- inventario de continuidade do Livro 1 em `02_ENREDOS_E_ESTRUTURAS/06_CONTINUIDADE_E_PAYOFFS/`
- dossie de estilo autoral em `04_DIRETRIZES_IA/DIRETRIZES/`
- sistema de roteamento estilistico em `04_DIRETRIZES_IA/DIRETRIZES/`
- matrizes de voz gramatical por POV em `04_DIRETRIZES_IA/DIRETRIZES/`
- engenharia textual e anti-padroes de IA em `04_DIRETRIZES_IA/DIRETRIZES/`
- 2 a 4 cenas revisadas e representativas de `03_CAPITULOS_E_CENAS/` ou da pasta local acentuada equivalente.

## Pacote Expandido

Adicionar quando a tarefa exigir continuidade fina:

- fichas individuais dos protagonistas;
- fichas individuais dos antagonistas;
- orbitais relevantes para a cena;
- plots por personagem em `02_ENREDOS_E_ESTRUTURAS/02_PLOTS_E_TRAMAS/`;
- estrutura do ato correspondente;
- timeline do ato correspondente;
- materiais sobre GLIF, Axsoma, transcendencia e paranormal;
- cenas anteriores e posteriores do mesmo capitulo.

## Prompt De Uso Para Claude

Quando o Drive ou Project Knowledge privado estiver conectado, Mario pode usar:

```text
Use o repositorio WildPoxx/veracrucia como camada publica de metodo e skills. Use a pasta privada de Veracrucia no Google Drive como fonte canonica quando estiver no Claude web. Se estiver em Claude Code/local com acesso ao filesystem, use C:\Users\amari\source\Veracrucia como raiz canonica local. Quando houver conflito, priorize: minhas instrucoes na conversa, cenas atuais, Biblia privada, estruturas de enredo, diretrizes de estilo e so depois a Biblia publica/GitHub. Antes de inventar qualquer fato, procure no material canonico ou marque como inferencia.
```

## Cuidados

- Nao enviar ao GitHub publico textos completos de capitulos sem decisao explicita de publicacao.
- Nao tratar indices como substitutos das fichas completas.
- Nao tratar a Biblia Publica como canon exaustivo.
- Nao deduzir destino de personagem apenas por funcao dramatica.
- Nao usar arquivos antigos ou backups como fonte superior se houver versao consolidada mais recente.
