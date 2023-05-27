# The box model (part 2)

## Parts of a box
* Making up a block box in CSS we have the:
    * Content box: The area where your content is displayed; size it using properties like inline-size and block-size or width and height.
    * Padding box: The padding sits around the content as white space; size it using padding and related properties.
    * Border box: The border box wraps the content and any padding; size it using border and related properties.
    * Margin box: The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using margin and related properties.
![img](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/box-model.png)

## Standard box
    * If we assume that a box has the following CSS:
  ```css
  .box {
  width: 350px;
  height: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}

  ```
  * The actual space taken up by the box will be 410px wide (350 + 25 + 25 + 5 + 5) and 210px high (150 + 25 + 25 + 5 + 5).
  ![img](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/standard-box-model.png)

## Margin
* The margin is an invisible space around your box. It pushes other elements away from the box. 
* Margins can have positive or negative values. Setting a negative margin on one side of your box can cause it to overlap other things on the page. 
* We can control all margins of an element at once using the margin property, or each side individually using the equivalent longhand properties:
    * margin-top
    * margin-right
    * margin-bottom
    * margin-left

## Borders
* The border is drawn between the margin and the padding of a box.
* For styling borders, there are a large number of properties — there are four borders, and each border has a style, width, and color that we might want to manipulate.
* You can set the width, style, or color of all four borders at once using the border property.
* To set the properties of each side individually, use:
  * border-top
  * border-right
  * border-bottom
  * border-left
* To set the width, style, or color of all sides, use:
  * border-width
  * border-style
  * border-color

## Padding
* The padding sits between the border and the content area and is used to push the content away from the border. 
* Unlike margins, you cannot have a negative padding. 
* Any background applied to your element will display behind the padding.
* To control each side individually, use these longhand properties:
    * padding-top
    * padding-right
    * padding-bottom
    * padding-left