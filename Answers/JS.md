# JavaScript Answers And External Sources
###<a name='q1'>Explain event delegation</a>

Event delegation allows you to avoid adding event listeners to specific nodes; 
instead, the event listener is added to one parent. 
That event listener analyzes bubbled events to find a match on child elements.

```html
<ul id="parent-list">
	<li id="post-1">Item 1</li>
	<li id="post-2">Item 2</li>
	<li id="post-3">Item 3</li>
	<li id="post-4">Item 4</li>
	<li id="post-5">Item 5</li>
	<li id="post-6">Item 6</li>
</ul>
```
```javascript
// Get the element, add a click listener...
document.getElementById("parent-list").addEventListener("click",function(e) {
	// e.target is the clicked element!
	// If it was a list item
	if(e.target && e.target.nodeName == "LI") {
		// List item found!  Output the ID!
		console.log("List item ",e.target.id.replace("post-")," was clicked!");
	}
});
```
### <a name='q2'>Explain how `this` works in JavaScript</a>
### <a name='q3'>Explain how prototypal inheritance works</a>
### <a name='q4'>How do you go about testing your JavaScript?</a>
### <a name='q5'>AMD vs. CommonJS?</a>
### <a name='q6'>What's a hashtable?</a>
###<a name='q7'> Explain why the following doesn't work as an IIFE: `function foo(){ }();`. 
    * What needs to be changed to properly make it an IIFE?</a>
###<a name='q8'> What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
    * How would you go about checking for any of these states?</a>
###<a name='q9'> What is a closure, and how/why would you use one?</a>
###<a name='q10'> What's a typical use case for anonymous functions?</a>
###<a name='q11'> Explain the "JavaScript module pattern" and when you'd use it.
   * Bonus points for mentioning clean namespacing.
   * What if your modules are namespace-less?</a>
###<a name='q12'> How do you organize your code? (module pattern, classical inheritance?)</a>
###<a name='q13'> What's the difference between host objects and native objects?</a>
###<a name='q14'> Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?</a>
###<a name='q15'> What's the difference between `.call` and `.apply`?</a>
###<a name='q16'> explain `Function.prototype.bind`?</a>
###<a name='q17'> When do you optimize your code?</a>
###<a name='q18'> Can you explain how inheritance works in JavaScript?</a>
###<a name='q19'> When would you use `document.write()`?</a>
###<a name='q20'> * Most generated ads still utilize `document.write()` although its use is frowned upon</a>
###<a name='q21'> What's the difference between feature detection, feature inference, and using the UA string</a>
###<a name='q22'> Explain AJAX in as much detail as possible</a>
###<a name='q23'> Explain how JSONP works (and how it's not really AJAX)</a>
###<a name='q24'> Have you ever used JavaScript templating?
    * If so, what libraries have you used? (Mustache.js, Handlebars etc.)</a>
###<a name='q25'> Explain "hoisting".</a>
###<a name='q26'> Describe event bubbling.</a>
###<a name='q27'> What's the difference between an "attribute" and a "property"?</a>
###<a name='q28'> Why is extending built in JavaScript objects not a good idea?</a>
###<a name='q29'> Why is extending built ins a good idea?</a>
###<a name='q30'> Difference between document load event and document ready event?</a>
###<a name='q31'> What is the difference between `==` and `===`?</a>
###<a name='q32'> Explain how you would get a query string parameter from the browser window's URL.</a>
###<a name='q33'> Explain the same-origin policy with regards to JavaScript.</a>
###<a name='q34'> Describe inheritance patterns in JavaScript.</a>

###<a name='q35'>Make this work:</a>
```javascript
[1,2,3,4,5].duplicate(); // [1,2,3,4,5,1,2,3,4,5]
```
```javascript
//Only add this implementation if one does not already exist.
if(Array.prototype.duplicate == null){
   Array.prototype.duplicate = function(){ return this.concat(this); }
}
```
###<a name='q36'> Describe a strategy for memoization (avoiding calculation repetition) in JavaScript.</a>
###<a name='q37'> Why is it called a Ternary expression, what does the word "Ternary" indicate?</a>
###<a name='q38'> What is the arity of a function?</a>
###<a name='q39'> What is `"use strict";`? what are the advantages and disadvantages to using it?</a>