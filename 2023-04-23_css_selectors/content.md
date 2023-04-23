# CSS Selectors

## Introduction
* In CSS, selectors are used to target the HTML elements on our web pages that we want to style.

## What is a selector?
* A CSS selector is a pattern of elements and other terms that tell the browser which HTML elements should be selected to have the CSS property values inside the rule applied to them. 
* The element or elements which are selected by the selector are referred to as the subject of the selector.

```css
h1{
    color: blue;
    background-color: yellow;
}
p{
    color: red;
}
```

## Selector lists
* If you have more than one thing which uses the same CSS then the individual selectors can be combined, by adding a comma, into a selector list so that the rule is applied to all of the individual selectors. 

```css
h1, h2 {
  color: blue;
}
```
* White space is valid before or after the comma. You may also find the selectors more readable if each is on a new line.
```css
h1,
h2 {
  color: blue;
}
```

## Type of selectors
* type:

```css
h1 {
}
```
* class:

```css
.box {
}
```
* id:

```css
#unique {
}
```

## Attribute selectors
* This group of selectors gives you different ways to select elements based on the presence of a certain attribute on an element

```css
a[title]
{
}
```
* Or even make a selection based on the presence of an attribute with a particular value

```css
a[href="https://example.com"]
{
}
```

## Pseudo-classes and pseudo-elements
* This group of selectors includes pseudo-classes, which style certain states of an element. The `:hover` pseudo-class for example selects an element only when it is being hovered over by the mouse pointer:
```css
a:hover {
}
```
* It also includes pseudo-elements, which select a certain part of an element rather than the element itself. For example, `::first-line` always selects the first line of text inside an element
```css
p::first-line {
}
```

