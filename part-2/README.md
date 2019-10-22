
# CSS Minis - Part 2: Positioning & Display


## SWBAT

* Differentiate between position properties (static, relative, absolute, fixed, sticky)
* Understand the basics of Flexbox & Grid


## Position Properties

* Static
  - Default property
  - Are not affected by the top, bottom, left, and right properties
* Relative
  - Positioned relative to it's normal position
  - The top, right, bottom, and left properties are used to position the element
* Absolute
  - Positioned relative to the nearest    positioned ancestor
  - When you assign a position to absolute it jumps out from the normal flow of the page
* Fixed
  - Positioned relative to the viewport - always stays in the same place even when page
    is scrolled
  - The top, right, bottom, and left properties are used to position the element
* Sticky
  - Positioned based on the user's scroll position

## Flexbox

One-dimensional system (row or column based)
- Flex Container
- Flex Items
- Main Axis
- Cross Axis

* Flex Container
- `display: flex || inline-flex` allows us to use flexbox in this container
- `flex-direction: column || row` defaults to column, dictates which direction flexbox goes
- `flex-wrap: nowrap || wrap` defaults to nowrap, dictates if we use single or multiple lines
- `flex-flow: row wrap` combines flex-wrap and flex-direction  
- `justify-content: flex-start || center || space-between || space-around  || space-evenly || flex-end` allows us to align items along the main axis of the current line of the flex-container (beginning of line, center, end, etc.)
- `align-items: stretch || flex-start || flex-end || center || baseline` similar to justify-content, but allows us to align items along the cross axis
-`align-content: stretch || flex-start || flex-end || center || space-between || space-around` similar to justify-content, but used when there is extra space on the cross axis

* Flex Items
- `order: 0 (number)` allows us to order elements in a row or column without changing the HTfML code
- `align-self: stretch || flex-start || flex-end || center || baseline` if you want to over ride the container alignment for one item
- `flex-grow: 0 (number)` define a size specific to that element
- `flex-basis: 1 (length)`  define a size specific to that element
- `flex-shrink: auto (number)`  define a size specific to that element
- `flex: 0 1 auto` grow, basis, shrink shortened to one line

Some properties of flexbox include:

justify-content - aligns items along the main axis
Can specify f - aligns items along the cross axis

Can specify:

flex-end, flex-start, center, baseline, stretch
flex-direction - choose the direction of items along the main axis

Can specify:

row, row-reverse, column, column-reverse
flex-wrap - choose whether items must remain on single lines or if they can wrap to new lines

Can specify:

nowrap, wrap, wrap-reverse
flex-flow - combines flex-direction and flex-wrap

You can also align specific flex items along the cross axis with align-self  

## Grid

Makes it easy to create well-designed and responsive pages

CSS Grid
Grid-based layout, two-dimensional system

Example makes dynamic auto-fill grid:

.image-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 10px;
}
Example makes 5 x 5 grid, where each column and each row is divided into 5 parts each filling 20% of the column and row, respectively:

.image-gallery {
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-rows: 20% 20% 20% 20% 20%;
  grid-gap: 10px;
}
Example makes 3x3 grid, where each column is divided into 3 fractional units and each row is divided into 3 fractional units:

.image-gallery {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  grid-gap: 10px;
}
grid-template is another way to generate your grid, and it combines both grid-template-columns and grid-template-rows

You can also target specific elements within the grid and specify where there should start/end via: grid-column-start, grid-column-end, grid-row-start, grid-row-end, grid-column, grid-row, grid-area

## Resources

- [Awwwards](https://www.awwwards.com/)
- [codrops](https://tympanus.net/codrops/css_reference/)
- [CSS Tricks](https://css-tricks.com/)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [CSS MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS Zen Garden](http://www.csszengarden.com/)
- [Flexbox Froggy](https://flexboxfroggy.com/)
- [CSS Grid Garden](http://cssgridgarden.com/)
- [DaFont](http://DaFont.com/)
- [Lost Type](http://losttype.com/)
