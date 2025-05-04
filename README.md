# CSS Flexbox
Este documento reúne os conhecimentos essenciais sobre Flexbox adquiridos durante os estudos. Traz explicações objetivas, trechos de código comentados e aplicações práticas para facilitar a visualização e domínio flexível em CSS.

---

## 📌 O que é CSS Flexbox?
Flexbox é um modelo de layout unidimensional do CSS que organiza itens dentro de um contêiner ao longo de um eixo principal (linha ou coluna). Ele distribui espaço entre os elementos de forma eficiente e oferece controle de alinhamento tanto no eixo principal quanto no eixo transversal, garantindo layouts responsivos mesmo quando o tamanho dos itens ou da tela muda.

---

## 🤔 Flexbox vs CSS Grid
O Flexbox é unidimensional, ideal para layouts em uma única linha ou coluna, enquanto o CSS Grid é bidimensional, permitindo layouts com linhas e colunas simultaneamente. O Flexbox é perfeito para distribuir espaço ao longo de um único eixo (horizontal ou vertical), enquanto o CSS Grid é ideal para layouts complexos que exigem controle sobre linhas e colunas.

| Flexbox           | CSS Grid             |
|-------------------|----------------------|
| Unidimensional    | Bidimensional        |
| Alinha em linha ou coluna | Alinha em linha **e** coluna |
| Melhor para componentes | Melhor para estruturas maiores |

## 📚 O que Foi Estudado?
### `01 - Flexbox`
Ativa o **Flexbox** e Define a direção dos itens em `linha` ou `coluna`.
```css
  .container {
    display: flex; /* Ativa o Flexbox */
    flex-direction: row; /* Define a direção em linha ou coluna */
  }
```

### `02 - Display Flex`
Esta propriedade define um flex container; `inline` ou `block` dependendo dos valores passados. Coloca todos os elementos-filhos diretos num contexto Flex.
```css
  .container {
    display: flex; /* or inline-flex */
  }
```

### `03 - Flex Direction`
Define o eixo principal, determinando a direção na qual os itens flexíveis (flex items) serão alinhados dentro do container. Ou seja, os itens são organizados em uma única linha ou coluna — horizontalmente ou verticalmente — dependendo da direção escolhida.
```css
  .flex-container {
    flex-direction: row | row-reverse | column | column-reverse;
  }
```

### `04 - Flex Wrap`
Por padrão, os flex items vão todos tentar se encaixar em uma só linha. Com esta propriedade você pode modificar esse comportamento e permitir que os ítens quebrem para uma linha seguinte conforme for necessário.
```css
  .flex-container {
    flex-wrap: nowrap | wrap | wrap-reverse;
  }
```

### `05 - Flex Flow`
É uma propriedade shorthand (uma mesma declaração inclui vários valores relacionados a mais de uma propriedade) que inclui `flex-direction` e `flex-wrap`. Determina quais serão os eixos pricipal e transversal do container. O valor padrão é `row nowrap`.
```css
  .flex-container {
    flex-flow: row nowrap | row wrap | column nowrap | column wrap;
  }
```

### `06 - Justify Content`
Esta propriedade define o alinhamento dos ítens ao longo do eixo principal.
```css
  .flex-container {
    justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
  }
```

### `07 - Align items`
Define o comportamento padrão de como flex items são alinhados de acordo com o eixo transversal (cross axis).
```css
  .flex-container {
    align-items: stretch | flex-start | flex-end | center | baseline;
  }
```

### `08 - Align Content`
Organiza as linhas dentro de um flex container quando há espaço extra no eixo transversal.
```css
  .flex-container {
    align-content: flex-start | flex-end | center | space-between | space-around | stretch;
  }
```

## Propriedades para elementos-filhos
A seguir, veremos propriedades que devem ser declaradas tendo como seletor os elementos-filhos:

### `09 - Flex Grow`
Define o quanto um item flexível pode crescer para ocupar o espaço disponível no container. Quanto maior o valor, maior a proporção de espaço que ele tenta ocupar em relação aos outros itens.
```css
  .flex-item {
    flex-grow: <numero>; /* o valor default(padrão) é 0 */
  }
```

### `10 - Flex Basis`
Define o tamanho inicial de um item flex antes de distribuir o espaço restante do container.
```css
  .flex-item {
    flex-basis: auto; /* o valor padrão é auto */
  }
```

### `11 - Flex Shrink`
Define a habilidade de um flex item de encolher, caso necessário.
```css
  .flex-item {
    flex-shrink: <número>; /* o valor padrão é 0 */
  }
```

### `12 - Flex`
Esta é a propriedade `shorthand` para `flex-grow`, `flex-shrink` e `flex-basis`, combinadas.
```css
  .item {
    flex: none [ <'flex-grow'> | <'flex-shrink'> | <'flex-basis'> ]
  }
```

### `13 - Order`
Determina a ordem em que os elementos aparecerão. Por padrão os flex items são dispostos na tela na ordem do código. Mas a propriedade `order` controla a ordem em que aparecerão no container.
```css
  .flex-item {
    order: <número>; /* o valor padrão é 0 */
  }
```

### `14 - Align Self`
Permite que o alinhamento padrão (ou o que estiver definido por align-items) seja sobrescrito para ítens individuais.
```css
  .item {
    align-self: auto | flex-start | flex-end | center | baseline | stretch;
  }
```
---

## 💡 Conclusão
O Flexbox é um módulo completo e não uma única propriedade; algumas delas devem ser declaradas no container (o elemento-pai, que chamamos de **flex container**), enquanto outras devem ser declaradas nos elementos-filhos (os **flex itens**).

## 📁 Estrutura deste repositório
```c#
📆 Flexbox - DevSamurai
🗂️ 01 - Flexbox
🗂️ 02 - Display Flex
🗂️ 03 - Flex Direction
🗂️ 04 - Flex Wrap
🗂️ 05 - Flex Flow
🗂️ 06 - Justify Content
🗂️ 07 - Align items
🗂️ 08 - Align Content
🗂️ 09 - Flex Grow
🗂️ 10 - Flex Basis
🗂️ 11 - Flex Shrink
🗂️ 12 - Flex
🗂️ 13 - Order
🗂️ 14 - Align Self
🗋 README.md
```

##### Feito com 💻 por **Matheus Souza** - [@SouzaStack](https://github.com/SouzaStack)