# CSS Layout

## Key Concepts in Positioning Elements
### Building Blocks CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box. Containing Elements If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

## block-level elements 
   * start on a new line ex: <**h1**> <**p**> <**ul**> <**li**>
## inline element   
   * flow in between suprouning text ex : <**img**> <**b**> <**i**>

   * CSS has the following positioning schemes that allow you to control the layout of a page:
     1. **Normal flow** (position:static) Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit  ide-byside, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).
     2. **Relative Positioning**  (position:relative)  This moves an element from the position it would be in normal flow, shifting it to the  op, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding  elements; they stay in the position they would be in in normal flow.
     3. **Absolute positioning** (position:absolute/fixed) This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

## clearing floats 
## clear 
### The clear property allows you to say that no element (within  the same containing element) should touch the left or right-hand sides of a box. It can take the following values:
* left 
   * The left-hand side of the box  should not touch any other elements appearing in the same containing element.
* right
   * The right-hand side of the box will not touch elements appearing in the same containing element.
* both
   * Neither the left nor right-hand sides of the box will touch elements appearing in the same containing element.
* none
   * Elements can touch either side.   

   ## Grid

1. define grid container element (parent) -> `display: grid`
2. set its column and row sizes -> `grid-template-columns` and `grid-template-rows`
3. place grid items (children) into the grid -> `grid-column` and `grid-row`

- children are only the direct descendants of the parent element
- _Note: column, float, clear, and vertical-align have no effect on a grid container._

### Terminology
1. grid container
2. grid item
3. grid line = The dividing lines that make up the structure of the grid.
4. grid track = column or row
5. grid cell = a single "unit" of the grid.
6. grid area = The total space surrounded by four grid lines. Can contain any number of cells.



