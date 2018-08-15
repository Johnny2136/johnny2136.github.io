---
layout: post
title: Day 13 of 100 Days Of Code
---

## Day 13: August 06, Monday

**Today 's Progress**: I worked on the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: I like these FCC_Challenges very straight forward I wish all were this way :grin:. Today it was all about Constructors and prototypes pretty cool stuff. Since today was such a good coding day I thought I would share my favorite cartoon series, enjoy!

![XKCD.com](https://imgs.xkcd.com/comics/disaster_movie.png)

```javascript
//Add Methods After Inheritance
//Add all necessary code so the Dog object inherits from Animal and the Dog's prototype constructor is set to Dog. Then add a bark() method to the Dog object so that beagle can both eat() and bark(). The bark() method should print "Woof!" to the console.
function Animal() { }
Animal.prototype.eat = function() { console.log("nom nom nom"); };
function Dog() { }
// Add your code below this line
Dog.prototype = Object.create(Animal.prototype);// my solution
Dog.prototype.constructor = Dog;// my solution
Dog.prototype.bark = function() {// my solution
  console.log( "Woof!");// my solution
};
// Add your code above this line
let beagle8 = new Dog();
beagle8.eat(); // Should print "nom nom nom"
beagle8.bark(); // Should print "Woof!"
console.log("--------------------------------------------");
```
and the last one my personal favorite `Mixin` :lol:
```javascript
//Use a Mixin to Add Common Behavior Between Unrelated Objects
//Create a mixin named glideMixin that defines a method named glide. Then use the glideMixin to give both bird and boat the ability to glide.
let bird = {
  name: "Donald",
  numLegs: 2
};
let boat = {
  name: "Warrior",
  type: "race-boat"
};
// Add your code below this line
let glideMixin = function(obj) {
  obj.glide = function() {
    console.log("Gliding, wooosh!");
  }
};
 glideMixin(bird);
 glideMixin(boat);
bird.glide(); // prints "Gliding, wooosh!"
boat.glide();
console.log(bird); // prints "Gliding, wooosh!"
console.log(boat); // prints "Gliding, wooosh!"
console.log("--------------------------------------------");
```
**Link(s) to work**

1. Continued [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedIterate Over All Properties
* PassedUnderstand the Constructor Property
* PassedChange the Prototype to a New Object
* PassedRemember to Set the Constructor Property when Changing the Prototype
* PassedUnderstand Where an Object’s Prototype Comes From
* PassedUnderstand the Prototype Chain
* PassedUse Inheritance So You Don't Repeat Yourself
* PassedInherit Behaviors from a Supertype
* PassedSet the Child's Prototype to an Instance of the Parent
* PassedReset an Inherited Constructor Property
* PassedAdd Methods After Inheritance
* PassedOverride Inherited Methods


All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)
