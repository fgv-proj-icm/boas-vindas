# Tutorial 04 — Ferramentas recomendadas

> **Para quem é este tutorial:** Membros que vão executar código (análises, pipelines, relatórios) nos projetos do Lab LEPP.

---

## Visão geral das ferramentas

| Ferramenta | Para quê usamos no Lab | Nível de exigência |
|---|---|---|
| **R** | Análise estatística, visualizações, relatórios reproduzíveis | Básico a avançado |
| **Python** | Pipelines de dados, automação, machine learning | Intermediário a avançado |
| **Quarto** | Relatórios científicos que combinam código + texto | Básico (após instalar) |
| **Git** | Controle de versão, sincronização com GitHub | Básico |

> **Você não precisa dominar tudo.** Cada projeto especifica o que é necessário no seu `README.md`.

---

## R — Instalação e configuração

### 1. Instalar o R

1. Acesse [cran.r-project.org](https://cran.r-project.org)
2. Clique em **"Download R for Windows"** (ou Mac/Linux conforme seu sistema)
3. Baixe e instale a versão mais recente

### 2. Instalar o RStudio (interface recomendada)

1. Acesse [posit.co/download/rstudio-desktop](https://posit.co/download/rstudio-desktop)
2. Baixe e instale o **RStudio Desktop** (versão gratuita)

### 3. Instalar pacotes usados no Lab

```r
# Pacotes de análise de dados
install.packages(c("tidyverse", "readxl", "janitor", "skimr"))

# Pacotes de visualização
install.packages(c("ggplot2", "plotly", "gt", "gtsummary"))

# Pacotes bibliométricos
install.packages("bibliometrix")

# Para relatórios Quarto
install.packages(c("knitr", "rmarkdown", "quarto"))
```

### 4. Primeiro passo em um projeto R

Cada projeto tem um arquivo `install_packages.R` na raiz. Abra o RStudio, navegue até a pasta do projeto e execute:

```r
source("install_packages.R")
```

---

## Python — Instalação e configuração

### 1. Instalar o Python

1. Acesse [python.org/downloads](https://www.python.org/downloads)
2. Baixe a versão **3.11 ou superior**
3. Na instalação, marque a opção **"Add Python to PATH"**

### 2. Configurar ambiente virtual (recomendado)

Dentro da pasta do projeto:

```bash
# Criar ambiente virtual
python -m venv .venv

# Ativar (Windows)
.venv\Scripts\activate

# Ativar (Mac/Linux)
source .venv/bin/activate

# Instalar dependências do projeto
pip install -r requirements.txt
```

### 3. VS Code como editor Python (recomendado)

1. Acesse [code.visualstudio.com](https://code.visualstudio.com)
2. Instale as extensões: **Python**, **Jupyter**, **Quarto**

### 4. Rodar um pipeline completo

Os projetos Python seguem o padrão:

```bash
# Verificar dependências
pip install -r requirements.txt

# Rodar pipeline completo
python -m nome_do_modulo.run --input data/raw --out outputs

# Ou via Makefile (se disponível)
make setup
make all
```

---

## Quarto — Relatórios científicos reproduzíveis

O **Quarto** é o padrão para relatórios do Lab LEPP. Ele combina texto em Markdown com código R ou Python e gera documentos em HTML, PDF ou Word.

### 1. Instalar o Quarto

1. Acesse [quarto.org/docs/get-started](https://quarto.org/docs/get-started/)
2. Baixe e instale para o seu sistema operacional

### 2. Renderizar um relatório

```bash
# Na pasta do projeto
quarto render nome-do-relatorio.qmd

# Especificando o formato de saída
quarto render nome-do-relatorio.qmd --to html
quarto render nome-do-relatorio.qmd --to pdf
quarto render nome-do-relatorio.qmd --to docx
```

### 3. Estrutura básica de um arquivo `.qmd`

```markdown
---
title: "Relatório Bibliométrico — Lab LEPP"
author: "Igor Caires Machado"
date: today
format: html
---

## Introdução

Este relatório apresenta os resultados...

```{r}
library(tidyverse)
dados <- read_csv("data/final/corpus.csv")
summary(dados)
```
```

---

## Git — Controle de versão pelo terminal

Para sincronizar seu trabalho com o GitHub sem usar a interface web:

```bash
# Verificar estado atual
git status

# Baixar atualizações do repositório remoto
git pull

# Adicionar arquivos alterados
git add nome-do-arquivo.R

# Salvar com descrição
git commit -m "atualiza análise exploratória — inclui variável de colegiado"

# Enviar para o GitHub
git push
```

### Quando algo der errado

```bash
# Ver o histórico de commits
git log --oneline

# Desfazer alterações em um arquivo (antes de fazer commit)
git checkout -- nome-do-arquivo.R

# Ver o que mudou em um arquivo
git diff nome-do-arquivo.R
```

---

## Configuração recomendada do VS Code para o Lab

Instale as extensões (disponíveis no arquivo `.vscode/extensions.json` já configurado):

- **Python** — suporte a Python e Jupyter
- **R** — suporte a R
- **Quarto** — suporte a `.qmd`
- **GitLens** — visualização avançada de histórico Git

---

## Preciso de ajuda com as ferramentas?

1. Abra uma [Issue](../../issues/new) descrevendo o problema
2. Especifique: sistema operacional, versão da ferramenta, e a mensagem de erro completa
3. Um membro da equipe irá ajudar

---

*[Voltar ao índice de tutoriais](README.md) · [Hub do Lab LEPP](../README.md)*
