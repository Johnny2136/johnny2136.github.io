---
layout: post
title: Day 15 of 100 Days Of Code
---

## Day 15: August, Wednesday

**Today 's Progress**: I continue to work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: These FCC_Challenges are pretty tricky, thank goodness for google! :grin:

![XKCD.com](https://imgs.xkcd.com/comics/bad_code.png)

```javascript
//Implement the filter Method on a Prototype
//Write your own Array.prototype.myFilter(), which should behave exactly like Array.prototype.filter(). You may use a for loop or the Array.prototype.forEach() method.
// the global Array
var s = [23, 65, 98, 5];
Array.prototype.myFilter = function(callback){
  var newArray = [];
  // Add your code below this line
   //console.log("this -->" + s);//Debug  
   this.forEach(function(obj) { //My solution
    //console.log("this -->" + obj);//Debug  
     if (callback(obj) == true) { //My solution
       newArray.push(obj); } });//My solution
      //console.log("this -->" + newArray);//Debug  
  // Add your code above this line
  return newArray;
};
var new_s = s.myFilter(function(item){
  return item % 2 === 1;
});
// Resources for this exercise: [Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `forEach` in conjunction with `callback`... [Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedImplement map on a Prototype
* PassedUse the filter Method to Extract Data from an Array
* PassedImplement the filter Method on a Prototype
* PassedReturn Part of an Array Using the slice Method to Extract Data from an Array


All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)
