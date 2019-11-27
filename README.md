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


 ### A Working Example:
 
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

## Events

All the different visitors' actions that a web page can respond to are called events. <br>

An event represents the precise moment when something happens. <br>

Examples:

moving a mouse over an element <br>
selecting a radio button <br>
clicking on an element <br>

Here are some common DOM events:

<table class="w3-table-all notranslate">
<tbody><tr>
<th style="width:23%">Mouse Events</th>
<th style="width:25%">Keyboard Events</th>
<th style="width:22%">Form Events</th>
<th>Document/Window Events</th>
</tr>
<tr>
<td>click</td>
<td>keypress</td>
<td>submit</td>
<td>load</td>
</tr>
<tr>
<td>dblclick</td>
<td>keydown</td>
<td>change</td>
<td>resize</td>
</tr>
<tr>
<td>mouseenter</td>
<td>keyup</td>
<td>focus</td>
<td>scroll</td>
</tr>
<tr>
<td>mouseleave</td>
<td>&nbsp;</td>
<td>blur</td>
<td>unload</td>
</tr>
</tbody></table>


### jQuery Syntax For Event Methods

To assign a click event to all paragraphs on a page, you can do this: <br>

$("p").click();

### Example: mouseenter() Event

The mouseenter() method attaches an event handler function to an HTML element.

The function is executed when the mouse pointer enters the HTML element:

```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("#p1").mouseenter(function(){
    alert("You entered p1!");
  });
});
</script>
</head>
<body>

<p id="p1">Enter this paragraph.</p>

</body>
</html>
```
### Example: blur() Event

The blur() method attaches an event handler function to an HTML form field. <br>

The function is executed when the form field loses focus:<br>



## JQuery Effects

### Example: jQuery hide() and show()
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("#hide").click(function(){
    $("p").hide();
  });
  $("#show").click(function(){
    $("p").show();
  });
});
</script>
</head>
<body>

<p>If you click on the "Hide" button, I will disappear.</p>

<button id="hide">Hide</button>
<button id="show">Show</button>

</body>
</html>
```

### Example: jQuery hide() and show() with controlling speed
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("#hide").click(function(){
    $("p").hide(1000);
  });
  $("#show").click(function(){
    $("p").show(1000);
  });
});
</script>
</head>
<body>

<p>If you click on the "Hide" button, I will disappear.</p>

<button id="hide">Hide</button>
<button id="show">Show</button>

</body>
</html>

```

###  Example: jQuery toggle()
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("p").toggle();
  });
});
</script>
</head>
<body>

<button>Toggle between hiding and showing the paragraphs</button>

<p>This is a paragraph with little content.</p>
<p>This is another small paragraph.</p>

</body>
</html>
```

### Example: jQuery fadeToggle() Method

The jQuery fadeToggle() method toggles between the fadeIn() and fadeOut() methods. <br>

If the elements are faded out, fadeToggle() will fade them in. <br>

If the elements are faded in, fadeToggle() will fade them out. <br>

```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("#div1").fadeToggle();
    $("#div2").fadeToggle("slow");
    $("#div3").fadeToggle(3000);
  });
});
</script>
</head>
<body>

<p>Demonstrate fadeToggle() with different speed parameters.</p>

<button>Click to fade in/out boxes</button><br><br>

<div id="div1" style="width:80px;height:80px;background-color:red;"></div>
<br>
<div id="div2" style="width:80px;height:80px;background-color:green;"></div>
<br>
<div id="div3" style="width:80px;height:80px;background-color:blue;"></div>

</body>
</html>
```

### Example: jQuery slideToggle() Method

The jQuery slideToggle() method toggles between the slideDown() and slideUp() methods. <br>

If the elements have been slid down, slideToggle() will slide them up. <br>
 
If the elements have been slid up, slideToggle() will slide them down. <br>

```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script> 
$(document).ready(function(){
  $("#flip").click(function(){
    $("#panel").slideToggle("slow");
  });
});
</script>
<style> 
#panel, #flip {
  padding: 5px;
  text-align: center;
  background-color: #e5eecc;
  border: solid 1px #c3c3c3;
}

#panel {
  padding: 50px;
  display: none;
}
</style>
</head>
<body>
 
<div id="flip">Click to slide the panel down or up</div>
<div id="panel">Hello world!</div>

</body>
</html>
```


### Example: jQuery animate()
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script> 
$(document).ready(function(){
  $("button").click(function(){
    var div = $("div");
    div.animate({height: '300px', opacity: '0.4'}, "slow");
    div.animate({width: '300px', opacity: '0.8'}, "slow");
    div.animate({height: '100px', opacity: '0.4'}, "slow");
    div.animate({width: '100px', opacity: '0.8'}, "slow");
  });
});
</script> 
</head>
<body>

<button>Start Animation</button>

<p>By default, all HTML elements have a static position, and cannot be moved. To manipulate the position, remember to first set the CSS position property of the element to relative, fixed, or absolute!</p>

<div style="background:#98bf21;height:100px;width:100px;position:absolute;"></div>

</body>
</html>
```

### jQuery Callback Functions
A callback function is executed after the current effect is finished. <br>
```html
Typical syntax: $(selector).hide(speed,callback);
```
### Example:
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide("slow", function(){
      alert("The paragraph is now hidden");
    });
  });
});
</script>
</head>
<body>

<button>Hide</button>

<p>This is a paragraph with little content.</p>

</body>
</html>
```

## Get Content - text(), html(), and val()
Three simple, but useful, jQuery methods for DOM manipulation are:

text() - Sets or returns the text content of selected elements
html() - Sets or returns the content of selected elements (including HTML markup)
val() - Sets or returns the value of form fields

The following example demonstrates how to get content with the jQuery text() and html() methods:
```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("#btn1").click(function(){
    alert("Text: " + $("#test").text());
  });
  $("#btn2").click(function(){
    alert("HTML: " + $("#test").html());
  });
});
</script>
</head>
<body>

<p id="test">This is some <b>bold</b> text in a paragraph.</p>

<button id="btn1">Show Text</button>
<button id="btn2">Show HTML</button>

</body>
</html>
```

## Set Content - text(), html(), and val()
We will use the same three methods from the previous page to set content:

text() - Sets or returns the text content of selected elements
html() - Sets or returns the content of selected elements (including HTML markup)
val() - Sets or returns the value of form fields
The following example demonstrates how to set content with the jQuery text(), html(), and val() methods:

```html
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $("#btn1").click(function(){
    $("#test1").text("Hello world!");
  });
  $("#btn2").click(function(){
    $("#test2").html("<b>Hello world!</b>");
  });
  $("#btn3").click(function(){
    $("#test3").val("Dolly Duck");
  });
});
</script>
</head>
<body>

<p id="test1">This is a paragraph.</p>
<p id="test2">This is another paragraph.</p>

<p>Input field: <input type="text" id="test3" value="Mickey Mouse"></p>

<button id="btn1">Set Text</button>
<button id="btn2">Set HTML</button>
<button id="btn3">Set Value</button>

</body>
</html>
```

