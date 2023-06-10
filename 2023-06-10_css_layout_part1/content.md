# CSS Layout

* CSS page layout techniques allow us to take elements contained in a web page and control where they're positioned relative to the following factors: 
  * their default position in normal layout flow
  * the other elements around them
  * their parent container
  * the main viewport/window

## Normal Flow
* Normal flow is how the browser lays out HTML element in the exact order in which it appears in the source code, with elements stacked on top of one another.
* The elements that appear one below the other are described as block elements, in contrast to inline elements, which appear beside one another like the individual words in a paragraph.
* The methods that can change how elements are laid out in CSS are: 
  * The `display` property
  * Floats
  * The `position` property
  * Table layout
  * Multi-colum layout

## Flexbox
* Flexbox is the short name for the Flexible Box Layout CSS module, designed to make it easy for us to lay things out in one dimension — either as a row or as a column.
* To use flexbox, you apply `display: flex` to the parent element of the elements you want to lay out; all its direct children then become flex items.
* As a simple example, we can add the `flex` property to all of our child items, and give it a value of `1`. This will cause all of the items to grow and fill the container, rather than leaving space at the end.


## Grid Layout
* While flexbox is designed for one-dimensional layout, Grid Layout is designed for two dimensions — lining things up in rows and columns
* Once you have a grid, you can explicitly place your items on it, rather than relying on the auto-placement behavior

```css
.box1 {
  grid-column: 2 / 4;
  grid-row: 1;
}

.box2 {
  grid-column: 1;
  grid-row: 1 / 3;
}

.box3 {
  grid-row: 2;
  grid-column: 3;
}
```

## Floats
* The floated element is moved to the left or right and removed from normal flow, and the surrounding content floats around it.

* The float property has four possible values:

  * left — Floats the element to the left.
  * right — Floats the element to the right.
  * none — Specifies no floating at all. This is the default value.
  * inherit — Specifies that the value of the float property should be inherited from the element's parent element.



