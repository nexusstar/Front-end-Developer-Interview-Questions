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

###<a name='q2'>Make this work:</a>
```javascript
[1,2,3,4,5].duplicate(); // [1,2,3,4,5,1,2,3,4,5]
```
```javascript
//Only add this implementation if one does not already exist.
if(Array.prototype.duplicate == null){
   Array.prototype.duplicate = function(){ return this.concat(this); }
}
```