
# Syntaxwear — Tênis e Sneakers Online

Projeto front-end estático que implementa a interface da loja "Syntaxwear": um layout responsivo para exibição de tênis e sneakers, com header fixo, hero, seções de categorias, grade de produtos e rodapé com newsletter.

## Tecnologias

- HTML5
- CSS3 (organizado em `css/` com variáveis e componentes)
- Google Fonts (`Ubuntu` via `css/variables.css`)

## Principais funcionalidades

- Cabeçalho fixo e responsivo com navegação principal e ícones de conta/ajuda/carrinho.
- Seção hero com imagem de destaque e CTA.
- Cards de categorias (Casual, Esporte, Moderno, Futurista).
- Grid de produtos responsivo usando CSS Grid e imagens de background.
- Rodapé com formulário de newsletter e links de navegação.
- Botões reutilizáveis com classes `btn`, `btn-outline` e `btn-filled`.

## Estrutura do projeto

- `index.html` — página principal (estrutura e marcação)
- `css/` — estilos base e componentes
	- `variables.css` — variáveis e import da fonte
	- `base.css` — estilos globais e classes utilitárias (`.btn`)
	- `components/` — estilos por componente (header, hero, product-grid, footer, etc.)
- `images/` — banners, logos, ícones e imagens de produtos

## Notas de implementação

- A tipografia utiliza a família `Ubuntu` importada em `css/variables.css`.
- O layout é responsivo com queries em componentes como `header`, `hero` e `product-grid`.
- As imagens são referenciadas em `images/` e usadas como `background-image` em cards da grade de produtos.

## Contribuição

- Para contribuir, crie uma issue descrevendo a sugestão ou bug e abra um pull request com mudanças claras.

## Licença

Sem licença explícita atualmente — adicione um arquivo `LICENSE` se desejar tornar o projeto público com termos específicos.

---