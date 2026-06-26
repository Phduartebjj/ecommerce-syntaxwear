# Checklist de Desenvolvimento (HTML + CSS — sem JS)

Este projeto segue uma estrutura de desenvolvimento focada em HTML semântico, CSS modular e boas práticas de acessibilidade, responsividade e organização.

---

## 0) Preparação do projeto

- Criar repositório (nome do projeto, licença, README inicial)
- Definir estrutura de pastas base:
/css
/images
/icons
/fonts
/favicons
/docs


- Criar arquivos iniciais:
  - `index.html`
  - `/css/base.css`
  - `/css/layout.css`

- Criar pasta de componentes CSS:
  - `/css/components/`

- Adicionar:
  - `.editorconfig`
  - `.gitignore` (node_modules, imagens brutas etc.)

- Definir design tokens em `/css/base.css`:
  - cores
  - tipografia
  - espaçamentos
  - radius
  - sombras

- Preparar placeholders de imagens:
  - logo
  - banner
  - 6–12 produtos

---

## 1) HTML — Esqueleto e landmarks

- Criar estrutura semântica no `index.html`:
  - `<header>`
  - `<nav>`
  - `<main>`
  - `<footer>`

- Adicionar “skip link” para o `<main>`

- Definir:
  - `<title>`
  - `lang`
  - `meta viewport`
  - `meta description`

- Planejar hierarquia de headings:
  - H1 na seção Destaque (Hero)
  - H2 nas demais seções

- Estruturar seções:
  - Painel informativo
  - Destaque (Hero)
  - Grid de produtos
  - Newsletter (no footer)

---

## 2) CSS Global (base)

- Normalização/reset leve em `base.css`
- Definir variáveis CSS (design tokens):
  - cores
  - fontes
  - espaçamentos
  - breakpoints

- Tipografia global:
  - body
  - headings
  - links
  - listas
  - parágrafos

- Utilitários:
  - `.container`
  - `.stack-*`
  - `.cluster`
  - `.grid-*`
  - `.sr-only`

- Definir tabela de breakpoints:
  - sm / md / lg / xl
  - helpers de media queries

---

## 3) CSS de Layout

- Definir largura máxima e gutters em `layout.css`
- Criar grids base responsivos
- Documentar uso de:
  - `.container`
  - `.stack`
  - `.cluster`

---

## 4) Header / Menu (HTML + CSS)

### HTML

- Logo
- Navegação principal
- Ações (login / cadastro)

### CSS (`/css/components/header.css`)

- Nomeclatura BEM leve:
  - `.site-header`
  - `.nav__list`
  - `.nav__link`

- Layout com Flexbox
- Estados:
  - hover
  - focus
  - ativo

- Responsividade:
  - mobile: navegação empilhada (sem JS)

- Acessibilidade:
  - `<nav>` com lista semântica
  - rótulos claros

---

## 5) Painel Informativo

### HTML

- Seção com USP:
  - frete
  - devolução
  - parcelamento

### CSS (`panel.css`)

- Layout com `.cluster` (ícone + texto)
- Responsivo:
  - empilhado no mobile
- Garantir contraste adequado

---

## 6) Destaque / Hero

### HTML

- H1
- Subtítulo
- CTA
- Imagem ou mídia de destaque

### CSS (`hero.css`)

- Layout com Grid ou Flex
- Possível sobreposição de texto
- Controle de legibilidade (claro/escuro)
- Responsividade:
  - ajuste de tipografia por breakpoint

---

## 7) Grid de Produtos

### HTML

- Lista de produtos
- Card de produto:
  - imagem
  - nome
  - preço
  - badge opcional

### CSS

#### `product-grid.css`

- Grid responsivo:
  - 2 col (sm)
  - 3 col (md)
  - 4 col (lg+)

#### `product-card.css`

- Layout em coluna (Flex)
- Espaçamentos consistentes
- Limite de texto (2 linhas)
- Aspect ratio:
  - 1:1 ou 4:5
- Estados:
  - `--sale`
  - `--new`

---

## 8) Footer + Newsletter

### HTML

- Links institucionais
- Ajuda / FAQ
- Redes sociais
- Formas de pagamento
- Newsletter

### CSS

#### `footer.css`

- Grid responsivo:
  - 1–2 col (mobile)
  - 3–4 col (desktop)

#### `newsletter.css`

- Label visível
- Input + botão
- Texto de ajuda

- Responsividade:
  - newsletter full-width no mobile

---

## 9) Acessibilidade essencial

- Apenas um H1 por página
- Hierarquia lógica de headings
- Alt text:
  - imagens informativas → descritivo
  - decorativas → `alt=""`
- Foco visível obrigatório
- Não remover outline sem substituto
- Contraste mínimo AA
- Alvos interativos ~44px
- Formulários:
  - labels explícitas
  - mensagens de ajuda/erro textuais

---

## 10) Responsividade e ajustes finais

- Testar breakpoints:
  - sm / md / lg / xl
- Ajustar:
  - tipografia
  - espaçamentos
  - gutters
- Testar navegadores:
  - Chrome
  - Firefox
  - Safari
- Testar diferentes viewports

---

## 11) Imagens e performance básica

- Otimizar imagens:
  - WebP / AVIF quando possível
- Definir `width` e `height` nas imagens
- Usar SVG para ícones quando aplicável
- Monitorar peso total da página

---

## 12) Organização e manutenção

- Revisar nomes de classes:
  - BEM leve + utilitários
- Remover CSS não utilizado
- Atualizar README com estrutura do projeto
- Criar guia curto de convenções em `/docs`
- Documentar design tokens e padrões CSS