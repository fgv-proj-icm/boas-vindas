<div align="center">

<img src="https://img.shields.io/badge/FGV_EPPG-Lab_LEPP-003087?style=for-the-badge&labelColor=1a1a2e" alt="Lab LEPP" height="40"/>

# Laboratório Experimental de Políticas Públicas

**FGV EPPG — Escola de Políticas Públicas e Governo · Brasília, Brasil**

[![Site Oficial](https://img.shields.io/badge/🌐_Site_Oficial-FGV_EPPG-003087?style=flat-square)](https://eppg.fgv.br/laboratorio-experimental-de-politicas-publicas-lab-lepp)
[![Drive do Lab](https://img.shields.io/badge/📁_Drive_do_Grupo-Google_Drive-4CAF50?style=flat-square)](https://drive.google.com/drive/folders/1B5o3vZmh4bRenAsdd9ZdHrbWxXnhEJPZ)
[![Voluntários](https://img.shields.io/badge/📋_Seja_Voluntário-Formulário-FF6600?style=flat-square)](https://docs.google.com/forms/d/e/1FAIpQLSe2KhEgf8uDZvgx0UskTPGe8ngI2Y6gYn5SwBIEElwsBfo50g/viewform)
[![Bolsas](https://img.shields.io/badge/🎓_Bolsas_Pós--Doc-CAPES-9C27B0?style=flat-square)](https://eppg.fgv.br/bolsas-de-estudos-lab-lepp)

</div>

---

> **Este é o repositório-hub do Lab LEPP.** Aqui você encontra o mapa de todos os projetos ativos, tutoriais para novos membros e os padrões de organização do laboratório.

---

## Índice rápido

| Para quem é novo | Para pesquisadores | Para colaboradores externos |
|:---:|:---:|:---:|
| [Primeiros passos →](tutoriais/01_primeiros-passos.md) | [Estrutura de projetos →](tutoriais/03_estrutura-projetos.md) | [Como contribuir →](tutoriais/02_baixar-e-contribuir.md) |

---

## Arquitetura de pesquisa ativa

O Lab LEPP organiza suas pesquisas em **linhas temáticas**. Dentro de cada linha, os projetos se conectam e se alimentam mutuamente.

```
LINHA: GOVERNANÇA JUDICIAL & PODER JUDICIÁRIO
│
├── [P1] Public_Policy ──────────► Bibliometria do campo
│         115 artigos nucleares        (revisão sistemática)
│                   │
│                   ▼
├── [P2] pjnp-avaliacao ─────────► Mapeamento das 40 PJNPs
│         tipologia + índices           (análise quantitativa)
│                   │
│                   ▼
└── [P3] artigo-3 ───────────────► Estudo comportamental (BPA)
          entrevistas + vinhetas        (pesquisa qualitativa)
                    │
                    ▼
          Submissão: Public Administration / JPART / RBAP
```

---

## Projetos por tipo de trabalho

### 📚 Revisão Bibliométrica

> Mapeamentos sistemáticos da literatura científica, análise de corpus, redes de co-citação.

| Repositório | Tema | Tecnologias | Status |
|---|---|---|:---:|
| [`Public_Policy/`](Public_Policy/) | Política judiciária e governança — 4.926 registros, pipeline completo | Python · R · Quarto | ✅ Consolidado |

---

### 📊 Análise Quantitativa

> Pipelines de dados, construção de índices, modelagem estatística, relatórios reproduzíveis.

| Repositório | Tema | Tecnologias | Status |
|---|---|---|:---:|
| [`pjnp-avaliacao/`](pjnp-avaliacao/) | Avaliação das 40 Políticas Judiciárias Nacionais Programáticas do CNJ | Python · R · Quarto | ✅ Consolidado |

---

### 🧪 Pesquisa Qualitativa & Experimental

> Experimentos comportamentais, entrevistas semiestruturadas, vinhetas instrumentais, análise temática.

| Repositório | Tema | Tecnologias | Status |
|---|---|---|:---:|
| [`artigo-3-final/`](artigo-3-final/) | Behavioral Public Administration — interpretação de indicadores por atores judiciais | Markdown · Atlas.ti | 🔄 Em andamento |

---

### 📝 Relatórios Técnicos e Notas de Política

> Notas técnicas, policy briefs, documentos para gestores públicos.

| Repositório | Tema | Destino | Status |
|---|---|---|:---:|
| *(em construção)* | — | — | — |

---

### 🏥 Saúde Pública

| Repositório | Tema | Tecnologias | Status |
|---|---|---|:---:|
| *(em construção)* | Letramento em saúde no DF | — | ⚪ Planejado |

---

### 💰 Economia Comportamental

| Repositório | Tema | Tecnologias | Status |
|---|---|---|:---:|
| *(em construção)* | Alfabetização financeira e vieses cognitivos | — | ⚪ Planejado |

---

## Status geral dos projetos

| Projeto | Pesquisador(es) | Início | Entregável | Status |
|---|---|---|---|:---:|
| Public_Policy | Igor Caires Machado | 2025 | Artigo bibliométrico | ✅ |
| pjnp-avaliacao | Igor Caires Machado | Abr/2026 | Artigo ENAJUS + RSP | ✅ |
| artigo-3-final | Marina Bonani · Antonio Melo Filho · Igor Caires Machado | Mai/2026 | Artigo BPA + Nota CNJ | 🔄 |

**Legenda:** ✅ Consolidado · 🔄 Em andamento · 🟡 Em revisão · ⚪ Planejado

---

## Para novos membros

Se você acabou de entrar no Lab LEPP, siga este caminho:

```
1. Leia os tutoriais abaixo (começa pelo 01)
2. Acesse o Drive do Grupo para documentos institucionais
3. Encontre o projeto da sua linha de pesquisa neste README
4. Leia o README.md dentro da pasta do projeto
5. Dúvidas? Abra uma Issue neste repositório
```

---

## Tutoriais

> Pasta [`tutoriais/`](tutoriais/) — guias passo a passo para todos os níveis de experiência com GitHub.

| # | Tutorial | Para quem |
|---|---|---|
| [01](tutoriais/01_primeiros-passos.md) | Primeiros passos no GitHub | Quem nunca usou a plataforma |
| [02](tutoriais/02_baixar-e-contribuir.md) | Como baixar e contribuir com arquivos | Todos os membros |
| [03](tutoriais/03_estrutura-projetos.md) | Estrutura padrão de projetos | Pesquisadores e RAs |
| [04](tutoriais/04_ferramentas.md) | Ferramentas recomendadas (R, Python, Quarto) | Quem vai rodar código |

---

## Links importantes

| Link | O que é |
|---|---|
| [🌐 Site do Lab LEPP](https://eppg.fgv.br/laboratorio-experimental-de-politicas-publicas-lab-lepp) | Página institucional — missão, projetos, equipe |
| [📁 Drive do Grupo](https://drive.google.com/drive/folders/1B5o3vZmh4bRenAsdd9ZdHrbWxXnhEJPZ) | Documentos, planilhas e arquivos de trabalho |
| [📋 Formulário de Voluntários](https://docs.google.com/forms/d/e/1FAIpQLSe2KhEgf8uDZvgx0UskTPGe8ngI2Y6gYn5SwBIEElwsBfo50g/viewform) | Participar como voluntário nas pesquisas do Lab |
| [🎓 Bolsas Pós-Doc](https://eppg.fgv.br/bolsas-de-estudos-lab-lepp) | Oportunidades CAPES e Pós-Doc Voluntário |

---

<div align="center">

*Dúvidas? Abra uma [Issue](../../issues/new) neste repositório.*

**Lab LEPP · FGV EPPG · Brasília, Brasil**

</div>
