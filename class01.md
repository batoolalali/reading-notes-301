# Responsive 
Responsive web design is the practice of building a website suitable to work on every device and every screen size.


### Responsive vs. Adaptive vs. Mobile
*Responsive* generally means to react quickly and positively to any change.
*Adaptive* means to be easily modified for a new purpose or situation, such as change.

**Flexible Layouts**
Responsive web design is broken down into three main components:
1. flexible layouts.
2. media queries.
3. flexible media.

*flexible layouts*
Website layouts need to adapt to this change and fixed values have too many constraints.

*media queries*
Media queries provide the ability to specify different styles for individual browser and device circumstances.

*flexible media*
equally important aspect to responsive web design involves flexible media. As viewports begin to change size media doesn’t always follow suit. Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

# Float
Float is a CSS positioning property.

### float values:
1. Left
2. Right
3. None (the default) ensures the element will not float
4. Inherit which will assume the float value from that elements parent element.

### What are floats used for?
- floats can be used to create entire web layouts.
- Floats are helpful for layout in smaller instances. 

### Clearing the Float
clear: both;	// to clear the float

- Both is most commonly used, which clears floats coming from either direction. 
- Left and Right can be used to only clear the float from one direction respectively. 
- None is the default, which is typically unnecessary unless removing a clear value from a cascade. 

### Techniques for Clearing Floats
- The Empty Div Method.
- The Empty Div Method.
- The Easy Clearing Method 

*The Easy Clearing Method*
```CSS
{
    .clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;

}
```
