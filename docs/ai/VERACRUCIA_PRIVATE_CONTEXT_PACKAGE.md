# Veracrucia Private Context Package

Este documento define o pacote privado recomendado para dar ao Claude acesso canonico amplo sem publicar o corpus completo no GitHub.

O pacote em si deve ser fornecido por Project Knowledge privado, Google Drive conectado, upload manual ou outra fonte controlada por Mario. Este arquivo no GitHub publico e apenas o guia de montagem e leitura.

## Regra Central

O repositorio publico `WildPoxx/veracrucia` contem metodo, skills e uma Biblia Publica controlada. O canon detalhado vive no vault privado:

```text
C:\Users\amari\source\Veracrucia
```

Se Claude tiver acesso ao Google Drive ou a arquivos anexados, deve tratar os arquivos abaixo como fontes canonicas, respeitando a ordem de precedencia.

## Ordem De Precedencia

1. Instrucoes diretas de Mario na conversa atual.
2. Capitulos/cenas atuais em `03_CAPÍTULOS_E_CENAS/`.
3. Biblia privada em `01_BIBLIA/`.
4. Estruturas de enredo e continuidade em `02_ENREDOS_E_ESTRUTURAS/`.
5. Diretrizes de estilo e IA em `04_DIRETRIZES_IA/`.
6. Skills e docs publicos do GitHub.
7. Inferencias do assistente, sempre marcadas como inferencias.

## Pacote Minimo Recomendado

Para dar contexto forte sem carregar tudo, incluir:

- `01_BIBLIA/index_biblia.md`
- `01_BIBLIA/01_PERSONAGENS/00_index_personagens_geral.md`
- `01_BIBLIA/02_LOCAIS_E_CENARIO/America Lusitania/⚙️ Veracrúcia.md`
- `01_BIBLIA/02_LOCAIS_E_CENARIO/Cidades/🦅 São Vicente — A Cidade do Ferro e do Sal*.md`
- `02_ENREDOS_E_ESTRUTURAS/03_ESTRUTURA_GERAL_DO_LIVRO/Matriz Crítica dos 3 Atos.md`
- `02_ENREDOS_E_ESTRUTURAS/06_CONTINUIDADE_E_PAYOFFS/Inventário de Continuidade - Livro 1*.md`
- `04_DIRETRIZES_IA/DIRETRIZES/Dossiê de Estilo Autoral - Veracrúcia.md`
- `04_DIRETRIZES_IA/DIRETRIZES/Sistema de Roteamento Estilistico - Core Veracrucia*.md`
- `04_DIRETRIZES_IA/DIRETRIZES/Matrizes de Voz Gramatical por POV - Veracrucia.md`
- `04_DIRETRIZES_IA/DIRETRIZES/Engenharia Textual e Anti-Padroes de IA.md`
- 2 a 4 cenas revisadas e representativas de `03_CAPÍTULOS_E_CENAS/`.

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
Use o repositorio WildPoxx/veracrucia como camada publica de metodo e skills. Use a pasta privada de Veracrucia no Google Drive como fonte canonica. Quando houver conflito, priorize: minhas instrucoes na conversa, cenas atuais, Biblia privada, estruturas de enredo, diretrizes de estilo e so depois a Biblia publica/GitHub. Antes de inventar qualquer fato, procure no material canonico ou marque como inferencia.
```

## Cuidados

- Nao enviar ao GitHub publico textos completos de capitulos sem decisao explicita de publicacao.
- Nao tratar indices como substitutos das fichas completas.
- Nao tratar a Biblia Publica como canon exaustivo.
- Nao deduzir destino de personagem apenas por funcao dramatica.
- Nao usar arquivos antigos ou backups como fonte superior se houver versao consolidada mais recente.
