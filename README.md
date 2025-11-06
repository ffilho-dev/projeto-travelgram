# Travelgram

Um layout estático de portfólio/galeria de viagens construído com HTML e CSS.

## Descrição

`Travelgram` é um template estático focado em apresentação visual de um perfil de viagens e uma galeria de fotografias. Foi desenvolvido com HTML sem frameworks e CSS modularizado, com atenção à clareza visual, manutenção e reutilização dos estilos. O projeto tem como objetivos:

- Mostrar um layout limpo e responsivo para apresentação de perfil e imagens.
- Separar responsabilidades de estilo para facilitar manutenção e escalabilidade.
- Utilizar variáveis CSS para centralizar tokens de design (cores, tipografia e espaçamentos).

O resultado é um projeto leve, ideal para demonstrativos, portfólios e como base para evoluções (ex.: adição de JavaScript ou integração a um CMS).

O projeto foi concebido com o objetivo primário de implementar e validar os conceitos operacionais do **modelo de layout Flexbox (CSS Flexible Box Layout Module)**.

### Técnicas de Flexbox

- Estruturação com containers flex (`display: flex`) para organizar o `header`, a barra de navegação e a galeria de imagens, garantindo alinhamento horizontal e vertical simples e previsível.
- Uso de propriedades-chave: `flex-direction`, `justify-content`, `align-items`, `gap`, `flex-wrap` e a propriedade shorthand `flex` (`flex-grow`, `flex-shrink`, `flex-basis`) para controlar comportamento de dimensionamento dos itens.
- `flex-wrap` combinado com breakpoints (media queries) para que a galeria e elementos do cabeçalho se reorganizem em telas menores sem alterar o DOM.
- Uso de `order` quando necessário para reordenar visualmente itens sem mudar a estrutura HTML, mantendo a separação entre conteúdo e apresentação.
- Integração com variáveis CSS: gaps, tamanhos e tokens de cor/tipografia são definidos em `:root` e reutilizados nas regras flex, permitindo ajustes globais rápidos.

### Por que usar Flexbox aqui (importância)

- Alinhamento e distribuição de espaço: Flexbox simplifica centragem e espaçamento entre elementos — operações que costumavam exigir hacks (floats, posicionamento absoluto) com maior complexidade.
- Responsividade nativa: a combinação `flex-wrap`, `flex-basis` e `gap` permite criar grades e filas que se adaptam ao tamanho da tela com poucas linhas de CSS.
- Código mais limpo e manutenível: ao aplicar o princípio de Single Responsibility nos arquivos de `styles/` (cada arquivo cuida de uma área), o uso de Flexbox mantém as regras locais e fáceis de entender e alterar.

Essas técnicas tornam o projeto uma boa base para evoluções futuras (ex.: adicionar grid CSS, animações, ou comportamento dinâmico via JavaScript) sem prejuízo da clareza ou da manutenção.

## Tecnologias

- HTML5
- CSS3
- Google Fonts (Poppins)

## Técnicas de CSS

- CSS Custom Properties (variáveis): o projeto centraliza cores, tipografia e espaçamentos em `:root` para facilitar ajustes e temas.
- Arquitetura por responsabilidade (Single Responsibility): cada arquivo em `styles/` tem uma responsabilidade única — por exemplo `global.css` para reset e variáveis, `header.css` para estilos do cabeçalho, `nav.css` para navegação, `main.css` para a galeria e `footer.css` para o rodapé. Isso reduz acoplamento entre áreas e facilita buscas e correções.
- Convenções e boas práticas: uso de classes utilitárias como `.container` e nomes semânticos.

## Estrutura de pastas

- `index.html` - página principal
- `assets/` - ícones, imagens e logos usados pelo site
  - `assets/icons/` - ícones (ex.: MapPin, AirplaneTilt, etc.)
  - `assets/images/` - imagens da galeria
- `styles/` - estilos CSS
  - `footer.css`, `global.css`, `header.css`, `index.css`, `main.css`, `nav.css`
