# Tutorial 02 — Como baixar e contribuir com arquivos

> **Para quem é este tutorial:** Todos os membros do Lab que precisam acessar ou adicionar arquivos aos repositórios.

---

## Baixar arquivos

### Opção A — Baixar um arquivo individual

1. Abra o arquivo desejado no repositório
2. Clique no botão **"Download raw file"** (ícone de download, canto superior direito)
3. O arquivo será salvo no seu computador

### Opção B — Baixar o repositório inteiro (ZIP)

1. Na página principal do repositório, clique no botão verde **"Code"**
2. Selecione **"Download ZIP"**
3. Extraia o arquivo no seu computador

> Use esta opção para ter todos os scripts e dados de um projeto de uma vez.

### Opção C — Clonar via terminal (para quem usa R ou Python)

```bash
git clone https://github.com/fgv-proj-icm/NOME-DO-REPOSITORIO.git
```

Isso cria uma cópia local conectada ao repositório — você pode sincronizar mudanças com `git pull`.

---

## Subir arquivos (contribuir)

### Subir um arquivo novo via interface web

1. Abra o repositório no GitHub
2. Navegue até a **pasta correta** onde o arquivo deve ficar
3. Clique em **"Add file" > "Upload files"**
4. Arraste ou selecione o(s) arquivo(s)
5. Escreva uma **mensagem descritiva** no campo "Commit message"
6. Clique em **"Commit changes"**

**Exemplos de boas mensagens de commit:**
```
adiciona script de análise descritiva — base PNAD 2023
atualiza roteiro de entrevista — revisão CEP
corrige cálculo do índice de maturidade — PJNP 07
```

> Evite mensagens genéricas como "update", "mudança" ou "arquivo novo".

---

### Editar um arquivo existente via interface web

1. Abra o arquivo no repositório
2. Clique no ícone de **lápis** (✏️) no canto superior direito
3. Faça suas alterações diretamente no editor do GitHub
4. Desça até o campo **"Commit changes"**
5. Escreva uma descrição do que foi alterado
6. Clique em **"Commit changes"**

---

### Subir arquivos via terminal (fluxo Git completo)

Para quem usa R, Python ou o terminal regularmente:

```bash
# 1. Entrar na pasta do projeto (após clonar)
cd nome-do-repositorio

# 2. Verificar o que mudou
git status

# 3. Adicionar arquivos ao próximo commit
git add nome-do-arquivo.R
git add .          # adiciona tudo (use com cuidado)

# 4. Criar o commit com descrição
git commit -m "adiciona análise exploratória — dados PJNP"

# 5. Enviar para o GitHub
git push
```

---

## O que NÃO subir ao repositório

| Tipo de arquivo | Por quê não subir | Alternativa |
|---|---|---|
| Dados brutos confidenciais (`.xlsx`, `.csv` com dados pessoais) | Privacidade e LGPD | Drive do grupo |
| Arquivos muito grandes (>100 MB) | Limite do GitHub | Drive do grupo + link |
| Credenciais, senhas, chaves de API | Segurança | Variáveis de ambiente (`.env`) |
| Transcrições de entrevistas com nomes | Ética em pesquisa | Pasta local criptografada |

> Os projetos do Lab já têm arquivos `.gitignore` configurados para bloquear automaticamente os tipos mais sensíveis.

---

## Próximo passo

[Tutorial 03 — Estrutura padrão de projetos →](03_estrutura-projetos.md)

---

*[Voltar ao índice de tutoriais](README.md) · [Hub do Lab LEPP](../README.md)*
