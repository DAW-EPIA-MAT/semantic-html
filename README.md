# CHALLENGE #00: SEMANTIC HTML

Semantics refers to the meaning of a piece of code

## Semantics in HTML

HTML should be coded to represent the data that will be populated and not based on its default presentation styling.

⚠️ Presentation (how it should look), is the sole responsibility of CSS.

In HTML there are a bunch of tags which are semantic elements. This means that a semantic tag gives the content it wraps around one defined role or meaning.

⚠️ Be careful! You could make any element look like a top level heading, but then it looses its semantic meaning.

```html
<!-- ✅ semantic tag -->
<h1>This is a top level heading</h1>
```

```html
<!-- ❌ non semantic tag.-->
<!-- It looks like an h1 element, but it's not-->
<h1>This is a top level heading</h1>
```

### Main semantic elements

There are a lot of sematic HTML elements, you can find them here. [ [MDN - HTML elements reference] ](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

Here you have a list with the main ones:

- article
- aside
- details
- figcaption
- figure
- footer
- form
- header
- main
- mark
- nav
- section
- summary
- time

### Semantics benefits

Some of the benefits from writing semantic markup are as follows:

- Search engines will consider its contents as important keywords to influence the page's search rankings (SEO)
- Screen readers can use it as a signpost to help visually impaired users navigate a page
- Finding blocks of meaningful code is significantly easier than searching through endless divs with or without semantic or namespaced classes
- Suggests to the developer the type of data that will be populated
- Semantic naming mirrors proper custom element/component naming

## Semantics in CSS

CSS responsability is defining presentational styles and view layout. But it also allows giving semantics to this presentational layer.

Consider styling a list with li elements representing different types of fruits. Would you know what part of the DOM is being selected with `div > ul > li`, or `.fruits__item`?

Using `id` and `class` will improve markup meaning.

### BEM (Block - Element - Modifier)

The Block, Element, Modifier methodology (BEM) is a popular naming convention for classes in HTML and CSS.

#### Block

A block is a top-level abstraction of a new component, for example a button.

Class can be defined as `class="btn"`, as far as this is the top-level component.

```html
<button class="btn">Subscribe</button>
```

#### Element

An element is the child item, or element, placed inside a block scope and it is denoted by two underscores following the name of the block, like `btn__price` or `btn__text`.

```html
<button class="btn">
  <span class="btn__price">$9.99</span>
  <span class="btn__text">Subscribe</span>
</button>
```

#### Modifier

Modifiers can manipulate the block so that we can theme or style that particular component without inflicting changes on a completely unrelated module.

This is done by appending two hyphens to the name of the block just like `btn--orange`.

```html
<button class="btn btn--big btn--orange">
  <span class="btn__price">$9.99</span>
  <span class="btn__text">Subscribe</span>
</button>
```

### Flex and grid

#### Flex

The Flexbox Layout (flex) module aims at providing a more efficient way to lay out, align and distribute space among items in a container (using one-directional flow), even when their size is unknown and/or dynamic.

You can practise Flex playing this [game](https://flexboxfroggy.com/#es).

#### Grid

CSS Grid Layout (grid), is a two-dimensional grid-based layout system that, compared to any web layout system of the past, completely changes the way we design user interfaces.

You can practise Grid playing this [game](https://cssgridgarden.com/#es).

---

### Source

- Semantics: https://developer.mozilla.org/en-US/docs/Glossary/Semantics
- BEM: https://css-tricks.com/bem-101/
- Flex (MDN): https://developer.mozilla.org/en-US/docs/Web/CSS/flex
- Flex (CSS Tricks): https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- Grid (MDN): https://developer.mozilla.org/en-US/docs/Web/CSS/grid
- Grid (CSS Tricks): https://css-tricks.com/snippets/css/complete-guide-grid/
