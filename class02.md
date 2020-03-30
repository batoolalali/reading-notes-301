# jQuery Overview 
- jQuery JavaScript library.
- You can download a copy of the jQuery library from www.jquery.com
-	Or include it from a CDN (Content Delivery Network)
**p.s We will use the CDN from the official jQuery website.**

- jQuery is a JavaScript library, so it has the .js file extension.
- In the html head we add ` <script src="https://code.jquery.com/jquery-3.1.1.js"></script>` to start using jQuery
- Ready: is an event is used to prevent any jQuery code from running before the document is finished loading.
```javaScript
{	
$(function() {
  $("#start").html("Go!");
});
}
```
// to change the content of the element which its id = start to Go!
**$ to access jQuery**

- jQuery syntax
`$("selector").action()`
-	$ to access jQuery
-	The (selector) finds HTML elements.
-	The action() is then performed on the element(s).
`$("p").hide()  // hides all <p> elements`
`$(".demo").hide()  // hides all elements with class="demo"`
`$("#demo").hide()  // hides the element with id="demo"`
- jQuery uses CSS syntax to select elements.


# Attributes and content

### Attributes
- ` var val = $("a").attr("href"); ` to get the value of an attribute.
- `$("a").attr("href", "http://www.jquery.com");` to set the attribute value
- The removeAttr() method is used for removing any attribute of an element.
 `$("table").removeAttr("border");`

### Content
- the html() method is used to get the content of the selected element
` var val = $("p").html();` it returns the content even there are tags inside this tag, it returns the tag

```javaScript
{
<p>
  JQuery is <b>fun</b>
</p>
}
```  
` var val = $("p").html();` returns `JQuery is <b>fun</b>`
`    var val = $("p").text();` returns JQuery is fun
` $("#test").text("hello!");` to set the text content 
` $("#demo").html("<b>Hi</b>");`  to change the content of the paragraphs with id="demo" to "<b>Hi</b>" maintaining the HTML markup.
- val() method, which allows us to get and set the values of form fields, such as textboxes, dropdowns, and similar inputs.
`var val= $("#name").val();`
- append() inserts content at the end of the selected elements.
- prepend() inserts content at the beginning of the selected elements.
- after() inserts content after the selected elements.
- before() inserts content before the selected elements.
`$("#demo").before("<i>Some Title</i>");`   
 ` $("#demo").after("<b>Welcome</b>");`
Add a tag before the p tag and after the p tag
- create new html element `var txt = $("<p></p>").text("Hi"); `
` $("#demo").after(txt);` to add the new element after the element which its id = demo


# Manipulating CSS

- Add class $("div").addClass("header");
`$("div").addClass("class1 class2 class3");` to specify multiple classes within the addClass() method 
- removeClass() method removes one or more class names from the selected elements.
- The toggleClass() method toggles between adding/removing classes from the selected elements if the specified class exists for the element, it is removed, and if it does not exist, it is added.
` $("p").toggleClass("red");`
- css() method can be used to get and set CSS property values.
`alert($("p").css("background-color"));` will alert with the p background color
`$("p").css("color", "blue");` to set the p font color
- You can specify any number of properties using this JSON syntax.
`$("p").css({"color": "red", "font-size": "200%"});`
- The width() and height() methods can be used to get and set the width and height of HTML elements.
`$("div").width(100);`
`$("div").height(100);`
- The innerWidth() and innerHeight() methods also include the padding.
- The outerWidth() and outerHeight() methods include the padding and borders.


# DOM
The DOM represents a document as a tree structure
HTML elements are interrelated nodes in the tree.
Nodes can have child nodes
Nodes on the same tree level are called siblings.
Traversing: is the term used to describe the process of moving through the DOM and finding (selecting) HTML elements based on their relation to other elements.
- The parent() method returns the direct parent element of the selected element
The parent() method can only traverse a single level up the DOM tree.
- parents() method. To get all ancestors of the selected element
- `$("div").eq(2);` if the page contains multiple div elements and we want to select the third one (specific index)
- remove() to remove selected elements from the DOM
- empty() method is used to remove the child elements of the selected element(s).


# Events
Events occur when the user performs an action, such as clicking an element, moving the mouse, or submitting a form.
When an event occurs on a target element, a handler function is executed.
``` javaScript
{
var x = document.getElementById("demo");
x.onclick = function () {
  document.body.innerHTML = Date();
}
}
```

### Common Events

-   Mouse Events:
    -	click occurs when an element is clicked.
    -	dblclick occurs when an element is double-clicked.
    -	mouseenter occurs when the mouse pointer is over (enters) the selected element.
    -	mouseleave occurs when the mouse pointer leaves the selected element.
    -	mouseover occurs when the mouse pointer is over the selected element.

-   Keyboard Events:
    -	keydown occurs when a keyboard key is pressed down.
    -	keyup occurs when a keyboard key is released.

-   Form Events:
    -	submit occurs when a form is submitted.
    -	change occurs when the value of an element has been changed.
    -	focus occurs when an element gets focus.
    -	blur occurs when an element loses focus.

-	Document Events:
    -	ready occurs when the DOM has been loaded.
    -	resize occurs when the browser window changes size.
    -	scroll occurs when the user scrolls in the specified element.


Another way to handle events in jQuery is by using the on() method.
```javascript
{
$( "p" ).on( "click", function() {
  alert("clicked");
});
}
```

You can remove event handlers using the off() method.
``` javaScript
{
$("div").on("click", function() { 
  alert('Hi there!'); 
  $("div").off("click");
});
}
```
### The Event Object
-   Every event handling function can receive an event object, which contains properties and methods related to the event
-	pageX, pageY the mouse position
-	type the type of the event
-	which the button or key that was pressed.
-	data any data that was passed in when the event was bound.
-	target the DOM element that initiated the event.
-	preventDefault() prevent the default action of the event (e.g., following a link).
-	stopPropagation() Stop the event from bubbling up to other elements.

-   trigger() method trigger events programmatically
``` javaScript
{
$(function() {
    $("#add").on("click", function() {
        var val = $("input").val();
        if(val !== '') {
            var elem = $("<li></li>").text(val);
            $(elem).append("<button class='rem'>X</button>");
            $("#mylist").append(elem);
            $("input").val("");
            $(".rem").on("click", function() {
                $(this).parent().remove();
            });
        }
    });
});
}
```


# Effects
- The hide() and show() methods are used to hide and show the selected elements.
- The toggle() method is used to toggle between hiding and showing elements.
If hidden >> show
If showed>>hide
*** The hide/show/toggle methods can take an optional argument, speed, which specifies the animation speed in milliseconds.
      `  $("div").toggle(1000);`
- fadeIn/fadeOut methods, which fade an element in and out of visibility.
- fadeToggle() method fades in and out.
- The slideUp() and slideDown() methods are used to create a sliding effect on elements.
- slideToggle() method switches between the sliding effects and can take two optional parameters: speed and callback.
- The animate() method lets you animate to a set value, or to a value relative to the current value.

```javaScript
{
$("div").click(function() {
  $("div").animate({width: '250px'}, 1000);
});
}
```
animates the width property of the div in 1 second to the value 250px
*** Multiple properties can be animated at the same time by separating them with commas.
*** To stop an animation before it is finished, jQuery provides the stop() method.
*** jQuery creates an "internal" queue for these method calls. Then it runs the animate calls one-by-one.


Book 193-301
jQuery doesn't do anything you cannot achieve with pure JavaScript. It is just a JavaScript file but estimates show it has been used on over a quarter of the sites on the web, because it makes coding simpler.
"Write less, do more”

Book 306-331
Looping:
when a selector returns multiple elements, you can update all of them using the one method. There is no need to use a loop.
CHAINING:
The process of placing several methods in the same selector is referred to as chaining
`$( 'li [id!="one"] ') .hide() .delay(5OO) . fadeln(1400);`

.replaceWith()   This method replaces every element in a matched set with new content. It also returns the replaced elements.
- jQuery allows you to recreate the functionality of a loop on a selection of elements, using the .each () method.
Allows you to perform one or more statements on each of the items in the selection of elements that is returned by a selector - rather like a loop in JavaScript.

``` javaScript
{
$( "li" ).each(function() {
  $( this ).addClass( "foo" );
});
}
```

# Pair Programming
- How does pair programming work?
pair programming commonly involves two roles: the Driver and the Navigator.
1.  Driver is the programmer who is typing and the only one whose hands are on the keyboard.
2. Navigator uses their words to guide the Driver but does not provide any direct input to the computer.

- Why pair program?
Pair programming touches on all four skills: 
1. developers explain out loud what the code should do.
2. listen to others’ guidance.
3. read code that others have written.
4. write code themselves.
