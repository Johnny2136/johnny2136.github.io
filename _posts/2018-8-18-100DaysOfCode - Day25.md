---
layout: post
title: Day 25 of 100 Days Of Code
---

## Day 25: August 18, Saturday

**Today 's Progress**: I completed work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: I focused on trying to understand the algorithm process and writing code. The Algorithms today were very complex, I once again had to rely on hints. I used the following resources in developing my solutions.

After searching and studying, I learned something new from the following:
* [Object.prototype.hasOwnProperty()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty)
* [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator),
* [Wikipedia Orbital Period](https://en.wikipedia.org/wiki/Orbital_period)
* [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),

```javascript
console.log("Map the Debris");
//Return a new array that transforms the elements' average altitude into their orbital periods (in seconds). The array will contain objects in the format {name: 'name', avgAlt: avgAlt}. You can read about orbital periods on [Wikipedia](https://en.wikipedia.org/wiki/Orbital_period). The values should be rounded to the nearest whole number. The body being orbited is Earth. The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.
function orbitalPeriod(arr) {
  const GM = 398600.4418;
  const earthRadius = 6367.4447;
  let a = 2 * Math.PI;
  let myArr = [];
  let getOrbPeriod = function(obj) {
    let c = Math.pow(earthRadius + obj.avgAlt, 3);
    let b = Math.sqrt(c / GM);
    let orbPeriod = Math.round(a * b);
    delete obj.avgAlt;
    obj.orbitalPeriod = orbPeriod;
    return obj;
  };
  for (var element in arr) {
    myArr.push(getOrbPeriod(arr[element]));
  }
  console.log(myArr);
  return myArr;
};
// test here
orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}]);
console.log("<----------------------next exercise------------------------->");
```
Once more I had to rely heavily on the hints when my first attempts failed. also [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) I can't say enough about this reference!

**Link(s) to work**

1. Finished [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedEverything Be True
* PassedArguments Optional
* PassedMake a Person
* PassedMap the Debris

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)
