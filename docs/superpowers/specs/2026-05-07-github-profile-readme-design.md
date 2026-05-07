# GitHub Profile README — Design Spec

**Data:** 2026-05-07  
**Autor:** Hian Claudio (W3SK3RRX)

---

## Objetivo

Redesenhar o `README.md` do perfil GitHub (`W3SK3RRX/W3SK3RRX`) para servir simultaneamente como:
- Portfólio técnico (mostrar projetos e stack)
- Cartão de visitas para recrutadores
- Ponto de networking com outros devs

---

## Decisões de Design

| Dimensão | Decisão |
|---|---|
| Estilo visual | Dark & Técnico (paleta escura, badges coloridos, visual de terminal) |
| Idiomas | Bilíngue — uma página com toggle 🇧🇷 PT / 🇺🇸 EN no topo |
| Layout | Duas colunas via tabela HTML (coluna esquerda + coluna direita) |

---

## Estrutura da Página

### Toggle de idioma (topo)
```
🇧🇷 Português | 🇺🇸 English
```
Links âncora que saltam para a seção `#português` ou `#english` dentro do mesmo arquivo.

---

### Bloco 🇧🇷 Português

#### Header centralizado
- Nome: **Hian Claudio**
- Animação de digitação via `readme-typing-svg` com as frases:
  - "Analista de Sistemas"
  - "Desenvolvedor Back-end"
  - "Python Developer"
  - "Fullstack Developer"
- Badges de status: `🇧🇷 Brasil` · `✅ Aberto a oportunidades` · `🚀 Back-end · Fullstack`

#### Layout duas colunas (tabela HTML)

**Coluna esquerda:**

1. **📌 Sobre mim** — bio de 3-4 linhas em tom técnico mas humano
2. **🛠️ Stack** — badges agrupados por categoria com cores temáticas:
   - Back-end: Python, Django, DRF, FastAPI → verde
   - Banco de dados: PostgreSQL, SQL → azul
   - DevOps & Cloud: Docker, GitHub, GitLab → roxo
   - Front-end: JavaScript, React, HTML5 → amarelo/laranja
3. **🔭 Atualmente** — lista com emoji:
   - 🔭 Trabalhando em...
   - 🌱 Aprendendo...
   - 💬 Me pergunte sobre Python, APIs, Docker
   - ⚡ Aberto a novos desafios

**Coluna direita:**

4. **📊 GitHub Stats** — três widgets empilhados:
   - `github-readme-stats` (stats gerais, theme: radical)
   - `github-readme-streak-stats` (sequência de commits)
   - `github-readme-stats` top-langs (layout: compact)
5. **🚀 Projetos em destaque** — 2-3 cards linkando os melhores repositórios, cada um com:
   - Nome do projeto
   - Descrição de 1 linha
   - Linguagem/stack principal
6. **📬 Contato** — LinkedIn, GitHub, e-mail

---

### Bloco 🇺🇸 English

Mesma estrutura do bloco PT, traduzida para inglês. Seções equivalentes:

| PT | EN |
|---|---|
| 📌 Sobre mim | 📌 About me |
| 🛠️ Stack | 🛠️ Tech Stack |
| 🔭 Atualmente | 🔭 Currently |
| 📊 GitHub Stats | 📊 GitHub Stats |
| 🚀 Projetos em destaque | 🚀 Featured Projects |
| 📬 Contato | 📬 Contact |

Os widgets de stats são compartilhados (mesmas URLs), sem duplicação desnecessária — apenas as seções de texto (bio, "atualmente", projetos) são traduzidas.

---

## Ferramentas & Serviços

| Ferramenta | Uso |
|---|---|
| [readme-typing-svg](https://readme-typing-svg.demolab.com) | Animação de digitação no header |
| [github-readme-stats](https://github.com/anuraghazra/github-readme-stats) | Stats gerais e top langs |
| [github-readme-streak-stats](https://streak-stats.demolab.com) | Streak de commits |
| [shields.io](https://shields.io) | Badges de tecnologia (style: for-the-badge) |

---

## Convenções Visuais

- **Paleta:** fundo `#0d1117`, texto `#c9d1d9`, destaques `#58a6ff` (azul) e `#3fb950` (verde)
- **Badges de tech:** `style=for-the-badge`, `color=000` (fundo preto), logo colorido
- **Separadores:** linha `---` entre blocos principais
- **Emojis:** usados como ícones de seção, não como decoração aleatória
- **Theme dos widgets:** `radical` para manter consistência dark

---

## O que NÃO incluir

- Contador de visitas ao perfil (descartado pelo usuário)
- GIFs ou animações pesadas além do typing-svg
- Informações pessoais além do necessário (sem endereço, telefone, etc.)

---

## Conteúdo a preencher (pelo usuário)

Antes da implementação, o usuário precisa definir:

1. **Bio curta** — 3-4 linhas descrevendo quem é, o que constrói e o que valoriza (PT e EN)
2. **"Atualmente"** — O que está trabalhando agora, o que está aprendendo (PT e EN)
3. **Projetos em destaque** — 2-3 repositórios com nome e descrição de 1 linha (PT e EN)

---

## Critérios de Sucesso

- [ ] Toggle de idioma funciona como âncora dentro da mesma página
- [ ] Animação de digitação exibe pelo menos 3 frases em loop
- [ ] Layout de duas colunas renderiza corretamente no GitHub (desktop)
- [ ] Todos os widgets de stats carregam com theme radical
- [ ] Badges de tech agrupados por categoria com cores distintas
- [ ] Seção PT e EN completas e consistentes
