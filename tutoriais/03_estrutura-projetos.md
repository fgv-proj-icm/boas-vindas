# Tutorial 03 — Estrutura padrão de projetos

> **Para quem é este tutorial:** Pesquisadores e assistentes de pesquisa que vão trabalhar dentro de um projeto do Lab LEPP.

---

## Por que ter uma estrutura padrão?

Quando todos os projetos seguem a mesma lógica de organização, qualquer membro do Lab consegue:
- Encontrar o que precisa sem pedir ajuda
- Retomar um projeto após semanas sem mexer nele
- Integrar dados e resultados de projetos diferentes
- Garantir que a pesquisa é reproduzível por outros pesquisadores

---

## Estrutura recomendada para projetos do Lab

```
nome-do-projeto/
│
├── README.md                  ← Apresentação do projeto (obrigatório)
│
├── 01_desenho/                ← Instrumentos e protocolo de pesquisa
│   ├── protocolo_etica.md
│   ├── roteiro_entrevista.md
│   └── instrumento_coleta.md
│
├── 02_dados/                  ← Dados brutos e processados
│   ├── raw/                   ← Dados originais (git-ignored se sensíveis)
│   └── processed/             ← Dados limpos, prontos para análise
│
├── 03_analise/                ← Scripts e código de análise
│   ├── 01_exploratory.R
│   ├── 02_modeling.py
│   └── livro_codigos.md       ← Para pesquisa qualitativa
│
├── 04_literatura/             ← Referências e notas de leitura
│   └── revisao_sintetica.md
│
├── 05_manuscrito/             ← Rascunhos e versões do artigo/relatório
│   ├── rascunho_v1.md
│   └── estrutura_artigo.md
│
├── docs/                      ← Decisões metodológicas, logs de progresso
│   ├── decisoes_metodologicas.md
│   └── log_progresso.md
│
└── outputs/                   ← Figuras, tabelas, relatórios gerados
    ├── figures/
    ├── tables/
    └── reports/
```

---

## Tipos de projetos e suas variações

### Revisão Bibliométrica (ex: `Public_Policy/`)

Inclui também:
- `data/raw/` — exportações das bases (Scopus, WoS, SciELO)
- `data/interim/` — dados em processamento (deduplicação, triagem)
- `data/final/` — corpus curado final
- `files_claude/` — scripts do pipeline automatizado
- `logs/` — registros do processo PRISMA

### Análise Quantitativa (ex: `pjnp-avaliacao/`)

Inclui também:
- `pjnp/` ou `src/` — código do pacote/módulo Python ou R
- `tests/` — testes automatizados
- `config/` — parâmetros e pesos configuráveis
- `writing/` — manuscritos e documentos de submissão

### Pesquisa Qualitativa (ex: `artigo-3-final/`)

Inclui também:
- `02_campo/transcricoes/` — **nunca versionado** (dados sensíveis)
- `03_analise/matrizes/` — matrizes analíticas cruzadas
- `03_analise/memos/` — memos analíticos durante codificação

---

## Convenções de nomenclatura

### Arquivos

| Tipo | Padrão | Exemplo |
|---|---|---|
| Scripts numerados | `NN_descricao.extensao` | `01_limpeza_dados.R` |
| Documentos | `descricao_versao.md` | `roteiro_entrevista_v2.md` |
| Dados brutos | `base_fonte_data.csv` | `pjnp_cnj_abr2026.xlsx` |
| Figuras | `fig_NN_descricao.png` | `fig_01_prisma_flow.png` |

### Pastas

- Use letras minúsculas e underscores: `minha_pasta/`
- Pastas numéricas para sequência lógica: `01_desenho/`, `02_dados/`
- Não use espaços, acentos ou caracteres especiais nos nomes

### Mensagens de commit

```
verbo + objeto + contexto

Exemplos:
  adiciona roteiro de entrevista — bloco D revisado
  corrige deduplicação — ajuste critério ISBN vs DOI  
  atualiza índice de maturidade — inclui colegiados nível 2
```

---

## Arquivo README.md obrigatório

Todo projeto deve ter um `README.md` na raiz com:

```markdown
# Nome do Projeto

**Pesquisador(es):** ...
**Instituição:** ...
**Início:** ...

## Objeto / Pergunta central

## Estrutura do repositório

## Como rodar (se houver código)

## Status atual
```

---

## Dados sensíveis e ética em pesquisa

- Dados com nomes reais de participantes **nunca entram no repositório**
- Use apenas os códigos: `P01`, `P02`, ... `P38` (ver protocolo ético do projeto)
- Transcrições ficam em pasta local, **fora** do repositório, criptografadas
- Arquivos `.gitignore` já estão configurados nos projetos para bloquear extensões sensíveis

---

## Próximo passo

[Tutorial 04 — Ferramentas recomendadas (R, Python, Quarto) →](04_ferramentas.md)

---

*[Voltar ao índice de tutoriais](README.md) · [Hub do Lab LEPP](../README.md)*
