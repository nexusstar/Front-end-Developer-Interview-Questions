# CSS Questions Answers And External Sources

###<a name='#q1'>Describe what a "reset" CSS file does and how it's useful.</a>

The CSS Reset __removes the inconsistent styling of HTML elements provided by browsers__.
 
This creates a dependably flat foundation to build upon.
 
The advantages for using "reset" CSS file are:
   
* They provide a blank canvas; any styles applied are (almost) certain to be your own.
* Development can be more logical: you’re adding styles rather than removing or modifying them.
* Browser compatibility issues can be minimized.

###<a name='#q2'>Describe Floats and how they work.</a>

__Float__ is a CSS positioning property.

Elements with the CSS float property applied to them are just like the images in the print layout where the text flows around them.

Floated elements remain a part of the flow of the web page.

There are four valid values for the float property.
 
* `Left` and `Right` float elements those directions respectively.
* `None` (the default) ensures the element will not float
* `Inherit` will assume the float value from that elements parent element.

Aside from the simple example of wrapping text around images, floats is used to create entire web layouts.

`clear` css property is used to specifies how to behave next to float element.
 
An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.
