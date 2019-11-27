# W02D04-Jquery

## JQuery

jQuery is a JavaScript Library. <br>

jQuery greatly simplifies JavaScript programming. <br>

jQuery is easy to learn. <br>


## What is jQuery?
jQuery is a lightweight, "write less, do more", JavaScript library. <br>

The purpose of jQuery is to make it much easier to use JavaScript on your website. <br>

jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code. <br>

jQuery also simplifies a lot of the complicated things from JavaScript, like AJAX calls and DOM manipulation. <br>

The jQuery library contains the following features:<br>

HTML/DOM manipulation<br>
CSS manipulation<br>
HTML event methods<br>
Effects and animations<br>
AJAX<br>

## Why jQuery?
There are lots of other JavaScript libraries out there, but jQuery is probably the most popular, and also the most extendable.

Many of the biggest companies on the Web use jQuery, such as:

Google <br>
Microsoft <br>
IBM <br>
Netflix <br>

## Adding jQuery to Your Web Pages

Download the jQuery library from jQuery.com <br>
```html
https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js
```

## Include the JQuery in your Web Pages

```html
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<head>
  ```
  
## What is a Minified file?
Minification refers to the process of removing unnecessary or redundant data without affecting how the resource is processed by the browser.<br>


 Example:
 
 ```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("p").click(function(){
    $(this).hide();
  });
});
</script>
</head>
<body>

<p>If you click on me, I will disappear.</p>
<p>Click me away!</p>
<p>Click me too!</p>

</body>
</html>
```



## jQuery Syntax
The jQuery syntax for selecting HTML elements and performing some action on the element(s).

```html
Basic syntax is: $(selector).action()
```

A $ sign to define/access jQuery <br>
A (selector) to "query (or find)" HTML elements <br>
A jQuery action() to be performed on the element(s) <br>


Examples:
```html
$(this).hide() - hides the current element.

$("p").hide() - hides all <p> elements.

$(".test").hide() - hides all elements with class="test".

$("#test").hide() - hides the element with id="test".
```


## The Document Ready Event
```html
$(document).ready(function(){

  // jQuery methods go here...

});
This is to prevent any jQuery code from running before the document is finished loading (is ready).
```

## jQuery Selectors
jQuery selectors allow you to select and manipulate HTML element(s). <br>

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more.

All selectors in jQuery start with the dollar sign and parentheses: $().

### The element Selector
The jQuery element selector selects elements based on the element name. <br>

You can select all <p> elements on a page like this:
```html
$("p")
 ```
  
  
Example:

When a user clicks on a button, all <p> elements will be hidden:
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide();
  });
});
</script>
</head>
<body>

<h2>This is a heading</h2>

<p>This is a paragraph.</p>
<p>This is another paragraph.</p>

<button>Click me to hide paragraphs</button>

</body>
</html>
```

<br>

### The #id Selector
The jQuery #id selector uses the id attribute of an HTML tag to find the specific element. <br>

An id should be unique within a page, so you should use the #id selector when you want to find a single, unique element. <br>

To find an element with a specific id, write a hash character, followed by the id of the HTML element:
```html
$("#test")
```

Example

When a user clicks on a button, the element with id="test" will be hidden:
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("#test").hide();
  });
});
</script>
</head>
<body>

<h2>This is a heading</h2>

<p>This is a paragraph.</p>
<p id="test">This is another paragraph.</p>

<button>Click me</button>

</body>
</html>
```

### The .class Selector
The jQuery .class selector finds elements with a specific class. <br>

To find elements with a specific class, write a period character, followed by the name of the class:
```html
$(".test")
```

Example

When a user clicks on a button, the elements with class="test" will be hidden:
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $(".test").hide();
  });
});
</script>
</head>
<body>

<h2 class="test">This is a heading</h2>

<p class="test">This is a paragraph.</p>
<p>This is another paragraph.</p>

<button>Click me</button>

</body>
</html>

```



