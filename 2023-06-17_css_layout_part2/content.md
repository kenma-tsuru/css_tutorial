# CSS Layout (part 2)


## Positioning Technique

* Positioning allows you to move an element from where it would otherwise be placed in normal flow over to another location.
* Positioning isn't a method for creating the main layouts of a page; it's more about managing and fine-tuning the position of specific items on a page.
* There are five types of positioning you should know about:
  * Static positioning (default, normal flow)
  * Relative positioning
  * Absolute positioning
  * Fixed positioning
  * Sticky positioning (skip)

### Relative positioning
* Relative positioning allows you to offset an item from its default position in normal flow.
* This means you could achieve a task such as moving an icon down a bit so it lines up with a text label. 


### Absolute positioning
* Absolute positioning is used to completely remove an element from the normal flow and instead position it using offsets from the edges of a containing block.


### Fixed positioning
* Fixed positioning removes our element from document flow in the same way as absolute positioning. However, instead of the offsets being applied from the container, they are applied from the viewport. 
* Because the item remains fixed in relation to the viewport, we can create effects such as a menu that remains fixed as the page scrolls beneath it.
