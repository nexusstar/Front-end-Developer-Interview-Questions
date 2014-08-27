# JavaScript Questions Answers And External Sources

###<a name='q1'>Make this work:</a>
```javascript
[1,2,3,4,5].duplicate(); // [1,2,3,4,5,1,2,3,4,5]
```
```javascript
//Only add this implementation if one does not already exist.
if(Array.prototype.duplicate == null){
   Array.prototype.duplicate = function(){ return this.concat(this); }
}
```