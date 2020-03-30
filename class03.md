# Javascript Templating Language with Mustache.js

### Javascript Templating
*Javascript templating* is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source.
The template is HTML markup, with added templating tags that will either insert variables or run programming logic.
The template engine then replaces variables and instances declared.

### Mustache
Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything.
- mustache.js is an implementation of the mustache template system in JavaScript. 

# A Guide to Flexbox
The Flexbox Layout aims at providing a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic.

The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.
- The flex container becomes flexible by setting the display property to flex.
```CSS
{
    .flex-container {
  display: flex;
}
}
```

- The flex container properties are:
    - flex-direction: defines in which direction the container wants to stack the flex items.
    - flex-wrap: specifies whether the flex items should wrap or not.
    - flex-flow: is a shorthand property for setting both the flex-direction and flex-wrap properties.
    - justify-content: is used to align the flex items.
    - align-items: is used to align the flex items vertically.
    - align-content: is used to align the flex lines.


- The direct child elements of a flex container automatically becomes flexible (flex) items.

- The flex item properties are:

 - order
 - flex-grow: specifies how much a flex item will grow relative to the rest of the flex items.
 - flex-shrink: specifies how much a flex item will shrink relative to the rest of the flex items.
 - flex-basis: specifies the initial length of a flex item.
 - flex: is a shorthand property for the flex-grow, flex-shrink, and flex-basis properties.
 - align-self: specifies the alignment for the selected item inside the flexible container.
 
### justify-content property which aligns items horizontally:
```CSS
{
#pond {
  display: flex;
justify-content: flex-end;
}
}
```

**justify-content accepts the following values**:
- flex-start: Items align to the left side of the container.
- flex-end: Items align to the right side of the container.
- center: Items align at the center of the container.
- space-between: Items display with equal spacing between them.
- space-around: Items display with equal spacing around them.

**aligns-items vertically and accepts the following values**:
 flex-start: Items align to the top of the container.
 flex-end: Items align to the bottom of the container.
 center: Items align at the vertical center of the container.
 baseline: Items display at the baseline of the container.
 stretch: Items are stretched to fit the container.

```CSS
{
  #pond {
  display: flex;
align-items:flex-end;
}
}
```

**flex-direction defines the direction items are placed in the container**
accepts the following values:
- row: Items are placed the same as the text direction.
- row-reverse: Items are placed opposite to the text direction.
- column: Items are placed top to bottom.
- column-reverse: Items are placed bottom to top.

**flex-wrap Spread items out**
accepts the following values:
- nowrap: Every item is fit to a single line.
- wrap: Items wrap around to additional lines.
- wrap-reverse: Items wrap around to additional lines in reverse.

The two properties **flex-direction** and **flex-wrap** are used so often together that the shorthand property **flex-flow** was created to combine them. This shorthand property accepts the value of one of the two properties separated by a space.


**align-content to set how multiple lines are spaced apart from each other**
this property takes the following values:
-  flex-start: Lines are packed at the top of the container.
-  flex-end: Lines are packed at the bottom of the container.
-  center: Lines are packed at the vertical center of the container.
-  space-between: Lines display with equal spacing between them.
-  space-around: Lines display with equal spacing around them.
-  stretch: Lines are stretched to fit the container.

