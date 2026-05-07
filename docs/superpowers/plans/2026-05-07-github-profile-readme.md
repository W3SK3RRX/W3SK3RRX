# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Redesenhar o `README.md` do perfil GitHub (W3SK3RRX) com estilo dark & técnico, bilíngue (PT/EN toggle), layout de duas colunas com animação de digitação, stack categorizada, stats completas e projetos em destaque.

**Architecture:** Um único arquivo `README.md` com dois blocos de conteúdo (PT e EN) separados por âncoras de navegação. Cada bloco usa uma tabela HTML de duas colunas — coluna esquerda com bio/stack/atualmente, coluna direita com stats/projetos/contato. Os widgets de stats da coluna direita só aparecem uma vez (no bloco PT); o bloco EN reutiliza a mesma seção via link interno.

**Tech Stack:** Markdown, HTML inline (tabela), readme-typing-svg, github-readme-stats, github-readme-streak-stats, shields.io

---

### Task 1: Gitignore + Esqueleto do README

**Files:**
- Modify: `.gitignore`
- Modify: `README.md`

- [ ] **Step 1: Adicionar `.superpowers/` ao `.gitignore`**

Abra `.gitignore` (ou crie se não existir) e adicione ao final:

```
# Brainstorm visual companion
.superpowers/
```

- [ ] **Step 2: Substituir o conteúdo completo do README pelo esqueleto abaixo**

```markdown
<!-- LANG TOGGLE -->
<div align="center">

[🇧🇷 Português](#português) &nbsp;|&nbsp; [🇺🇸 English](#english)

</div>

---

<a name="português"></a>

## 🇧🇷 Versão em Português

<!-- PT CONTENT AQUI -->

---

<a name="english"></a>

## 🇺🇸 English Version

<!-- EN CONTENT AQUI -->
```

- [ ] **Step 3: Verificar renderização**

Abra o arquivo no GitHub (após push) ou use um previewer local. Confirme que os dois links do toggle aparecem no topo e clicam para as seções corretas.

- [ ] **Step 4: Commit**

```bash
git add .gitignore README.md
git commit -m "chore: setup README skeleton and gitignore"
```

---

### Task 2: Bloco PT — Header com animação

**Files:**
- Modify: `README.md` (substituir `<!-- PT CONTENT AQUI -->`)

- [ ] **Step 1: Adicionar header centralizado com typing animation**

Substitua `<!-- PT CONTENT AQUI -->` por:

```markdown
<div align="center">

### 👋 Olá! Eu sou o Hian Claudio

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Analista+de+Sistemas;Desenvolvedor+Back-end;Python+Developer;Fullstack+Developer)](https://git.io/typing-svg)

![](https://img.shields.io/badge/🇧🇷_Brasil-000?style=flat-square)
![](https://img.shields.io/badge/✅_Aberto_a_oportunidades-000?style=flat-square&color=3fb950)
![](https://img.shields.io/badge/🚀_Back--end_·_Fullstack-000?style=flat-square&color=58a6ff)

</div>
```

- [ ] **Step 2: Verificar a animação**

Abra a URL abaixo no navegador para confirmar que a animação funciona e as frases rodam corretamente:

```
https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Analista+de+Sistemas;Desenvolvedor+Back-end;Python+Developer;Fullstack+Developer
```

Deve exibir um SVG animado com as 4 frases em loop.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat(readme): add PT header with typing animation"
```

---

### Task 3: Bloco PT — Duas colunas (esquerda: bio + stack + atualmente)

**Files:**
- Modify: `README.md` (adicionar após o header PT)

- [ ] **Step 1: Adicionar abertura da tabela HTML e coluna esquerda**

Logo após o bloco do header PT, adicione:

```markdown
<table>
<tr>
<td width="50%" valign="top">

### 📌 Sobre mim

<!-- PREENCHA: 3-4 linhas descrevendo quem você é, o que constrói e o que valoriza -->
Analista de Sistemas apaixonado por construir **APIs robustas** e sistemas escaláveis.
Trabalho principalmente com **Python, Django e FastAPI**, sempre buscando boas práticas e código limpo.
Acredito que boa tecnologia resolve problemas reais — e que clareza no código é respeito ao próximo dev.

---

### 🛠️ Stack

**Back-end**

![Python](https://img.shields.io/badge/Python-000?style=for-the-badge&logo=python&logoColor=3fb950)
![Django](https://img.shields.io/badge/Django-000?style=for-the-badge&logo=django&logoColor=3fb950)
![DRF](https://img.shields.io/badge/DRF-000?style=for-the-badge&logo=django&logoColor=3fb950)
![FastAPI](https://img.shields.io/badge/FastAPI-000?style=for-the-badge&logo=fastapi&logoColor=3fb950)

**Banco de dados**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-000?style=for-the-badge&logo=postgresql&logoColor=58a6ff)
![SQL](https://img.shields.io/badge/SQL-000?style=for-the-badge&logo=sqlite&logoColor=58a6ff)

**DevOps & Cloud**

![Docker](https://img.shields.io/badge/Docker-000?style=for-the-badge&logo=docker&logoColor=d2a8ff)
![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=d2a8ff)
![GitLab](https://img.shields.io/badge/GitLab-000?style=for-the-badge&logo=gitlab&logoColor=d2a8ff)

**Front-end**

![JavaScript](https://img.shields.io/badge/JavaScript-000?style=for-the-badge&logo=javascript&logoColor=ffd700)
![React](https://img.shields.io/badge/React-000?style=for-the-badge&logo=react&logoColor=ffd700)
![HTML5](https://img.shields.io/badge/HTML5-000?style=for-the-badge&logo=html5&logoColor=ff7b00)

**Outros**

![Linux](https://img.shields.io/badge/Linux-000?style=for-the-badge&logo=linux)
![Figma](https://img.shields.io/badge/Figma-000?style=for-the-badge&logo=figma)

---

### 🔭 Atualmente

<!-- PREENCHA: substitua os exemplos abaixo com o que você está fazendo de verdade -->
- 🔭 Trabalhando em **projetos com Django REST Framework**
- 🌱 Aprendendo **arquitetura de microsserviços**
- 💬 Me pergunte sobre **Python, APIs REST, Docker**
- ⚡ Sempre aberto a **novos desafios e colaborações**

</td>
```

- [ ] **Step 2: Verificar badges no navegador**

Abra algumas URLs de badge para confirmar que os logos carregam:

```
https://img.shields.io/badge/Python-000?style=for-the-badge&logo=python&logoColor=3fb950
https://img.shields.io/badge/Docker-000?style=for-the-badge&logo=docker&logoColor=d2a8ff
```

Ambas devem retornar imagens de badge com fundo preto e logo colorido.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat(readme): add PT left column - bio, stack, currently"
```

---

### Task 4: Bloco PT — Duas colunas (direita: stats + projetos + contato)

**Files:**
- Modify: `README.md` (adicionar coluna direita e fechar tabela)

- [ ] **Step 1: Adicionar coluna direita e fechar a tabela**

Logo após o `</td>` da coluna esquerda, adicione:

```markdown
<td width="50%" valign="top">

### 📊 GitHub Stats

![Hian's GitHub Stats](https://github-readme-stats.vercel.app/api?username=W3SK3RRX&show_icons=true&theme=radical&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=3fb950)

![GitHub Streak](https://streak-stats.demolab.com?user=W3SK3RRX&theme=radical&hide_border=true&background=0d1117&ring=58a6ff&fire=ff7b00&currStreakLabel=58a6ff)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=W3SK3RRX&layout=compact&theme=radical&hide_border=true&bg_color=0d1117&title_color=58a6ff)

---

### 📬 Contato

[![LinkedIn](https://img.shields.io/badge/LinkedIn-000?style=for-the-badge&logo=linkedin&logoColor=0A66C2)](https://www.linkedin.com/in/hian-claudio/)
[![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github)](https://github.com/W3SK3RRX)

📩 hianclaudio16@gmail.com

</td>
</tr>
</table>
```

- [ ] **Step 2: Verificar URLs dos widgets**

Abra no navegador para confirmar que os widgets carregam (podem demorar alguns segundos):

```
https://github-readme-stats.vercel.app/api?username=W3SK3RRX&show_icons=true&theme=radical&hide_border=true&bg_color=0d1117
https://streak-stats.demolab.com?user=W3SK3RRX&theme=radical&hide_border=true&background=0d1117
https://github-readme-stats.vercel.app/api/top-langs/?username=W3SK3RRX&layout=compact&theme=radical&hide_border=true&bg_color=0d1117
```

Cada URL deve retornar uma imagem SVG com dados reais do usuário W3SK3RRX.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat(readme): add PT right column - stats, contact"
```

---

### Task 5: Bloco EN — Header + Duas colunas completas

**Files:**
- Modify: `README.md` (substituir `<!-- EN CONTENT AQUI -->`)

- [ ] **Step 1: Adicionar bloco EN completo**

Substitua `<!-- EN CONTENT AQUI -->` por:

```markdown
<div align="center">

### 👋 Hey there! I'm Hian Claudio

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Systems+Analyst;Back-end+Developer;Python+Developer;Fullstack+Developer)](https://git.io/typing-svg)

![](https://img.shields.io/badge/🇧🇷_Brazil-000?style=flat-square)
![](https://img.shields.io/badge/✅_Open_to_work-000?style=flat-square&color=3fb950)
![](https://img.shields.io/badge/🚀_Back--end_·_Fullstack-000?style=flat-square&color=58a6ff)

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📌 About me

<!-- PREENCHA: tradução da bio para inglês -->
Systems Analyst passionate about building **robust APIs** and scalable systems.
I work primarily with **Python, Django and FastAPI**, always aiming for best practices and clean code.
I believe good technology solves real problems — and that clear code is a sign of respect for the next developer.

---

### 🛠️ Tech Stack

**Back-end**

![Python](https://img.shields.io/badge/Python-000?style=for-the-badge&logo=python&logoColor=3fb950)
![Django](https://img.shields.io/badge/Django-000?style=for-the-badge&logo=django&logoColor=3fb950)
![DRF](https://img.shields.io/badge/DRF-000?style=for-the-badge&logo=django&logoColor=3fb950)
![FastAPI](https://img.shields.io/badge/FastAPI-000?style=for-the-badge&logo=fastapi&logoColor=3fb950)

**Database**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-000?style=for-the-badge&logo=postgresql&logoColor=58a6ff)
![SQL](https://img.shields.io/badge/SQL-000?style=for-the-badge&logo=sqlite&logoColor=58a6ff)

**DevOps & Cloud**

![Docker](https://img.shields.io/badge/Docker-000?style=for-the-badge&logo=docker&logoColor=d2a8ff)
![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=d2a8ff)
![GitLab](https://img.shields.io/badge/GitLab-000?style=for-the-badge&logo=gitlab&logoColor=d2a8ff)

**Front-end**

![JavaScript](https://img.shields.io/badge/JavaScript-000?style=for-the-badge&logo=javascript&logoColor=ffd700)
![React](https://img.shields.io/badge/React-000?style=for-the-badge&logo=react&logoColor=ffd700)
![HTML5](https://img.shields.io/badge/HTML5-000?style=for-the-badge&logo=html5&logoColor=ff7b00)

**Other**

![Linux](https://img.shields.io/badge/Linux-000?style=for-the-badge&logo=linux)
![Figma](https://img.shields.io/badge/Figma-000?style=for-the-badge&logo=figma)

---

### 🔭 Currently

<!-- PREENCHA: tradução do "atualmente" para inglês -->
- 🔭 Working on **Django REST Framework projects**
- 🌱 Learning **microservices architecture**
- 💬 Ask me about **Python, REST APIs, Docker**
- ⚡ Always open to **new challenges and collaborations**

</td>
<td width="50%" valign="top">

### 📊 GitHub Stats

![Hian's GitHub Stats](https://github-readme-stats.vercel.app/api?username=W3SK3RRX&show_icons=true&theme=radical&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=3fb950)

![GitHub Streak](https://streak-stats.demolab.com?user=W3SK3RRX&theme=radical&hide_border=true&background=0d1117&ring=58a6ff&fire=ff7b00&currStreakLabel=58a6ff)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=W3SK3RRX&layout=compact&theme=radical&hide_border=true&bg_color=0d1117&title_color=58a6ff)

---

### 📬 Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-000?style=for-the-badge&logo=linkedin&logoColor=0A66C2)](https://www.linkedin.com/in/hian-claudio/)
[![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github)](https://github.com/W3SK3RRX)

📩 hianclaudio16@gmail.com

</td>
</tr>
</table>
```

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat(readme): add EN section with full bilingual structure"
```

---

### Task 6: Revisão final e push

**Files:**
- Review: `README.md`

- [ ] **Step 1: Verificar estrutura geral do arquivo**

Confirme que o README tem esta ordem:

```
[toggle PT | EN]
---
## 🇧🇷 Versão em Português
  [header centralizado + typing]
  [tabela 2 colunas PT]
---
## 🇺🇸 English Version
  [header centralizado + typing]
  [tabela 2 colunas EN]
```

- [ ] **Step 2: Verificar todos os links de âncora**

Teste manualmente os dois links do toggle após push:
- `#português` deve saltar para a seção PT
- `#english` deve saltar para a seção EN

- [ ] **Step 3: Push para o GitHub**

```bash
git push origin main
```

- [ ] **Step 4: Verificar o perfil no GitHub**

Abra `https://github.com/W3SK3RRX` no navegador e confirme:
- [ ] Toggle PT/EN visível no topo
- [ ] Animação de digitação funcionando no header PT
- [ ] Animação de digitação funcionando no header EN
- [ ] Badges de stack com cores corretas em ambas as colunas
- [ ] Stats, streak e top-langs carregando com theme radical
- [ ] Links de contato clicáveis

---

## Notas de Conteúdo

Decisão durante o brainstorm: usar o conteúdo default escrito nas tasks (bio e "atualmente"). O usuário pode editar manualmente depois se quiser personalizar — os marcadores `<!-- PREENCHA: ... -->` ficam como hint não-renderizado.
