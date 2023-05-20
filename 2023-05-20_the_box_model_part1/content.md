# The box model (part 1)
* Everything in CSS has a box around it, and understanding these boxes is key to being able to create more complex layouts with CSS, or to align items with other items.

## Block and inline boxes
* In CSS we have several types of boxes that generally fit into the categories of **block** boxes and **inline** boxes. 
* The type refers to how the box behaves in terms of page flow and in relation to other boxes on the page. 
* Boxes have an **inner display** type and an **outer display** type.
* In general, you can set various values for the display type using the `display` property, which can have various values.

## Outer display type
* If a box has an outer display type of block, then:
    * The box will break onto a new line.
    * The `width` and `height` properties are respected.
    * Padding, margin and border will cause other elements to be pushed away from the box.
    * If width is not specified, the box will extend in the inline direction to fill the space available in its *container*. 
    * In most cases, the box will become as wide as its container, filling up 100% of the space available.

* If a box has an outer display type of inline, then:
    * The box will not break onto a new line.
    * The `width` and `height` properties will not apply.
    * Top and bottom padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
    * Left and right padding, margins, and borders will apply and will cause other inline boxes to move away from the box.

## Inner display type
* Boxes also have an inner display type, which dictates how elements **inside that box** are laid out.
* By default and without any other instruction, the elements inside a box are also laid out in normal flow and behave as block or inline boxes.
* When you move on to learn about CSS Layout in more detail, you will encounter flex, and various other inner values that your boxes can have, for example grid.