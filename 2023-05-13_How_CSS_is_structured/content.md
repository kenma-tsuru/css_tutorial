# How CSS is Structured

## Applying CSS to HTML

### External stylesheet
* An external stylesheet contains CSS in a separate file with a `.css` extension.
* You reference an external CSS stylesheet from an HTML `<link>` element. The href attribute of the `<link>` element needs to reference a file on your file system.
```html
<!DOCTYPE html>
<html lang="en-GB">
  <head>
    <meta charset="utf-8" />
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

### Internal stylesheet
* An internal stylesheet resides within an HTML document. 
* To create an internal stylesheet, you place CSS inside a `<style>` element contained inside the HTML tag.
```html
<!DOCTYPE html>
<html lang="en-GB">
  <head>
    <meta charset="utf-8" />
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```
* For sites with more than one page, an internal stylesheet becomes a less efficient way of working. To apply uniform CSS styling to multiple pages using internal stylesheets, you must have an internal stylesheet in every web page that will use the styling. 

### Inline styles
* Inline styles are CSS declarations that affect a single HTML element, contained within a `style` attribute.

```html
<!DOCTYPE html>
<html lang="en-GB">
  <head>
    <meta charset="utf-8" />
    <title>My CSS experiment</title>
  </head>
  <body>
    <h1 style="color: blue;background-color: yellow;border: 1px solid black;">
      Hello World!
    </h1>
    <p style="color:red;">This is my first CSS example</p>
  </body>
</html>
```
* Avoid using CSS in this way, when possible. Inline CSS mixes (CSS) presentational code with HTML and content, making everything more difficult to read and understand. Separating code and content makes maintenance easier for all who work on the website.

## Selectors

### Specificity
* The CSS language has rules to control which selector is stronger in the event of a conflict. 
* These rules are called `cascade` and `specificity`. 
* In the code block below, we define two rules for the `p` selector, but the paragraph text will be blue. 
* This is because the declaration that sets the paragraph text to blue appears later in the stylesheet. 
* Later styles replace conflicting styles that appear earlier in the stylesheet. This is the **cascade rule**.
```css
p {
  color: red;
}

p {
  color: blue;
}
```
```html
<p class="special">What color am I?</p>
```

* However, in the case of our earlier example with the conflict between the *class* selector and the *element* selector, the class prevails, rendering the paragraph text red. 
* A class is rated as being more *specific*, as in having more **specificity** than the element selector, so it cancels the other conflicting style declaration.

```css
.special {
  color: red;
}


p {
  color: blue;
}
```
```html
<p class="special">What color am I?</p>
```

## Properties and values

* CSS properties and values are case-insensitive. The property and value in a property-value pair are separated by a colon (:).
* If a property is unknown, or if a value is not valid for a given property, the declaration is processed as invalid. It is completely ignored by the browser's CSS engine.

## Functions
* The `calc()` function, which can do simple math within CSS
```css
.outer {
  border: 5px solid black;
}

.box {
  padding: 10px;
  width: calc(90% - 30px);
  background-color: rebeccapurple;
  color: white;
}
```
```html
<div class="outer"><div class="box">The inner box is 90% - 30px.</div></div>
```

## @rule
* CSS @rules (pronounced "at-rules") provide instruction for what CSS should perform or how it should behave. Some @rules are simple with just a keyword and a value.
```css
@import "styles2.css";
```
* One common @rule that you are likely to encounter is `@media`, which is used to create media queries. 
* Media queries use conditional logic for applying CSS styling.
* In the example below, the stylesheet defines a default pink background for the `<body>` element. However, a media query follows that defines a blue background if the browser viewport is wider than 30em.

```css
body {
  background-color: pink;
}

@media (min-width: 30em) {
  body {
    background-color: blue;
  }
}
```

## Shorthands
* Some properties like `font`, `background`, `padding`, `border`, and `margin` are called shorthand properties. This is because shorthand properties set several values in a single line.

```css
/* In 4-value shorthands like padding and margin, the values are applied
   in the order top, right, bottom, left (clockwise from the top). There are also other
   shorthand types, for example 2-value shorthands, which set padding/margin
   for top/bottom, then left/right */
padding: 10px 15px 15px 5px;
```
```css
padding-top: 10px;
padding-right: 15px;
padding-bottom: 15px;
padding-left: 5px;
```

## Whitespace
* White space means actual spaces, tabs and new lines. Just as browsers ignore white space in HTML, browsers **ignore** white space inside CSS. The value of white space is how it can improve readability.
