---
layout: post
title: Day 14 of 100 Days Of Code
---

## Day 14: August, Tuesday

**Today 's Progress**: I finished the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section and started [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Oh no these FCC_Challenges are not at all straight forward, and there are no hints or examples it's very challenging and not a lot of fun Thank goodness there is google! You can really tell the folks who did the last round of challenges cared about passing on information rather than this round of challenges designed to trick the student and make things obscure and nerve wracking. Today it was all about dealing with these frustrating misleading challenges yuck!

![XKCD.com](https://imgs.xkcd.com/comics/code_quality.png)

```javascript
//Implement map on a Prototype
//Write your own Array.prototype.myMap(), which should behave exactly like Array.prototype.map(). You may use a for loop or the forEach method.
// the global Array
var s = [23, 65, 98, 5];
Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
   for (let i = 0; i < this.length; i++) {
     newArray.push(callback(this[i]));
  };
  // Add your code above this line
  return newArray;
};
var new_s = s.myMap(function(item){
  return console.log(item * 2);
});
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out callback...

**Link(s) to work**

1. Continued [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedUse a Mixin to Add Common Behavior Between Unrelated Objects
* PassedUse Closure to Protect Properties Within an Object from Being Modified Externally
* PassedUnderstand the Immediately Invoked Function Expression (IIFE)
* PassedUse an IIFE to Create a Module

2. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedLearn About Functional Programming
* PassedUnderstand Functional Programming Terminology
* PassedUnderstand the Hazards of Using Imperative Code
* PassedAvoid Mutations and Side Effects Using Functional Programming
* PassedPass Arguments to Avoid External Dependence in a Function
* PassedRefactor Global Variables Out of Functions
* PassedUse the map Method to Extract Data from an Array


All code is in GitHub and repl.it here: [Repl.it OOP](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming), [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub OOP](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js), [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)
