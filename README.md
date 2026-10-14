# Portfólio Pessoal | Gabriel Ribeiro Rodrigues

Site de portfólio pessoal em página única (one page), feito com HTML e CSS puros, como atividade de layout com **CSS Grid** e **Flexbox**.

- **Aluno:** Gabriel Ribeiro Rodrigues
- **Curso:** Análise e Desenvolvimento de Sistemas, Senac-MG
- **Site publicado:** [PREENCHER COM O LINK DO GITHUB PAGES]
- **Repositório:** https://github.com/grrtsu/portfolio

## Prints

### Desktop

![Versão desktop do portfólio](img/print-desktop.png)

### Mobile

![Versão mobile do portfólio](img/print-mobile.png)

## Seções

| Seção | id | Conteúdo |
|---|---|---|
| Cabeçalho | (header) | Logo e menu com links âncora para todas as seções |
| Sobre | `#sobre` | Foto, nome, área de interesse e apresentação |
| Habilidades | `#habilidades` | 3 cards (Front-End, SQL e Python) com etiquetas |
| Projetos | `#projetos` | 4 cards com imagem, título, descrição e link |
| Formação e Experiência | `#formacao` | Linha do tempo de formação e de experiência |
| Contato | `#contato` | Links de e-mail, LinkedIn e GitHub e formulário visual |
| Rodapé | (footer) | Direitos autorais, ano e links rápidos |

## Onde usei CSS Grid

| Elemento | Seletor | Como |
|---|---|---|
| Seção Sobre | `.sobre` | `grid-template-columns: auto 1fr` com `gap`: foto em uma coluna, texto na outra |
| Cards de Habilidades | `.card-hab` | `grid-template-columns: repeat(3, 1fr)` com `gap` |
| Galeria de Projetos | `.projetos-grid` | `grid-template-columns: repeat(4, 1fr)` com `gap` |
| Formação e Experiência | `.card-form` | `grid-template-columns: repeat(2, 1fr)` com `gap` |

Nos breakpoints, os grids diminuem o número de colunas (por exemplo, Projetos passa de 4 para 2 colunas no tablet e para 1 no celular).

## Onde usei Flexbox

| Elemento | Seletor | Como |
|---|---|---|
| Cabeçalho | `.cabeca` | `justify-content: space-between` e `align-items: center` entre o logo e o menu; vira coluna no celular |
| Menu de navegação | `.menu` | Links lado a lado com `gap` e `justify-content: flex-end` |
| Card de habilidade | `.card-hab article` | `flex-direction: column` com `gap`; `flex-grow: 1` no texto deixa as etiquetas no fim do card |
| Etiquetas | `.card-hab ul` | Itens lado a lado com `flex-wrap: wrap` e `gap` |
| Card de projeto | `.projetos-grid article` e `.card-link` | `flex-direction: column` organizando imagem, título e texto |
| Contato | `.contato` | Links e formulário lado a lado (`flex-direction: row`), virando coluna no celular (`flex-direction: column`) |
| Lista de contatos | `.contato-links` e `.meio-contato` | Lista em coluna; cada contato com `justify-content: space-between` |
| Formulário | `.form-contato` | Campos em coluna com `gap` |
| Rodapé | `.rodape` | `justify-content: space-between`, `align-items: center` e `flex-wrap` |

## Responsividade

O site tem 2 breakpoints, feitos com `@media (max-width: ...)` no fim do `style.css`:

**Até 992px (tablet)**
- Habilidades e Projetos passam para 2 colunas (`repeat(2, 1fr)`)
- A seção Sobre vira uma coluna só, com a foto centralizada em cima do texto

**Até 600px (celular)**
- Todos os grids (Habilidades, Projetos e Formação) ficam com 1 coluna
- O cabeçalho muda de `flex-direction: row` para `column`: logo em cima, menu embaixo, com `flex-wrap` nos links
- A seção Contato muda de `flex-direction: row` para `column`: links em cima, formulário embaixo
- O rodapé muda para `flex-direction: column`, centralizado
- Margens laterais menores e textos alinhados à esquerda, para ler melhor em tela estreita

## Organização

- CSS em arquivo externo (`css/style.css`), sem CSS inline
- Cores e fontes em variáveis no `:root`
- Comentários separando cada seção do CSS
- Fontes: Bricolage Grotesque (títulos) e IBM Plex Sans (texto), do Google Fonts

```
portfolio/
├── index.html
├── README.md
├── css/
│   └── style.css
└── img/
```

## Uso de Inteligência Artificial

Usei o **Claude (Anthropic)** como apoio durante o desenvolvimento, conforme permitido pela atividade. Todo o código foi digitado, testado e ajustado por mim, e sei explicar cada trecho.

**Explicações e tira-dúvidas:** conceitos de HTML semântico, diferença entre Grid e Flexbox, unidades (`rem`, `fr`, `%`), especificidade e ordem das regras no CSS, comandos de Git e solução de um problema no VS Code.

**Revisão do meu código:** a IA apontou erros que eu corrigi, como a vírgula em `grid-template-columns`, os `<li>` que faltavam no menu, `div` sem fechar e um seletor com vírgula que afetava o site inteiro.

**Trechos de código sugeridos pela IA** (que eu adaptei ao meu projeto):

- Centralização das seções com `max-width` e `margin: 0 auto`
- Cabeçalho fixo com `position: sticky` e efeito de vidro (`backdrop-filter`)
- Imagens dos cards de projeto (`width: 100%`, `object-fit: cover`, `overflow: hidden`) e efeito de hover
- Card do S.I.M.P.I.U. inteiro clicável (`.card-link`)
- HTML e CSS da linha do tempo da seção Formação e Experiência
- Linha divisória entre as seções (`section + section`)
- HTML e CSS da seção Contato (lista de links e formulário)
- CSS do rodapé
- Media queries de responsividade (tablet e celular)

**Conteúdo:**

- Sugestão das fontes e da paleta de cores
- Revisão e reescrita dos textos dos cards de Habilidades
- Descrição do projeto S.I.M.P.I.U., escrita a partir do documento e do Figma do projeto de extensão
- Os projetos **Calculadora POO**, **Painel Dado Crítico** e **Taverna RPG** são fictícios: nomes, descrições e imagens foram criados pela IA. A imagem do S.I.M.P.I.U. é uma tela do Figma do projeto.
