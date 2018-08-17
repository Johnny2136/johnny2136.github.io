---
layout: post
title: Day 23 of 100 Days Of Code
---

## Day 24: August 17, Friday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: After a very long week I am finally able to relax a bit I took today off so I could focus on resting and writing code. So the Algorithms today were a mixed bag, some easier than others. I used the following resources in developing my solutions.

After searching and studying, I learned something new from the following:
* [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
* [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex),
* [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator),
* [JavaScript Operators](https://www.w3schools.com/js/js_operators.asp)
* [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),

```javascript
console.log("Drop it");
//Given the array arr, iterate through and remove each element starting from the first element (the 0 index) until the function func returns true when the iterated element is passed through it. Then return the rest of the array once the condition is satisfied, otherwise, arr should be returned as an empty array.
//Resources to solve this: [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex), [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator), [JavaScript Operators](https://www.w3schools.com/js/js_operators.asp), [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),
function dropElements(arr, func) {
  console.log(arr.slice(arr.findIndex(func) >= 0
    ? arr.findIndex(func): arr.length, arr.length));//Used for debugging
  return arr.slice(arr.findIndex(func) >= 0
    ? arr.findIndex(func): arr.length, arr.length);
};
// test here
dropElements([1, 2, 3, 4], function(n) {return n >= 3;});
console.log("<----------------------next exercise------------------------->");

console.log("Steamroller");
//Flatten a nested array. You must account for varying levels of nesting.
function steamrollArray(arr) {
  let myArr = [].concat(...arr);
  console.log(myArr);//Debugging
  //console.log(myArr.some(Array.isArray) ? steamrollArray(myArr) : myArr);//Debugging
  return myArr.some(Array.isArray)
    ? steamrollArray(myArr) : myArr;
   //console.log(myArr); //Debugging
};
// test here
steamrollArray([[["a"]], [["b"]]]);// should return ["a", "b"].
steamrollArray([1, [2], [3, [[4]]]]);// should return [1, 2, 3, 4].
steamrollArray([1, [], [3, [[4]]]]);// should return [1, 3, 4].
steamrollArray([1, {}, [3, [[4]]]]);// should return [1, {}, 3, 4].
console.log("<----------------------next exercise------------------------->");
```
I still find myself having to rely heavily on the hints and [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) I can't say enough about this reference!

**Link(s) to work**

1. Continuing [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedDrop it
* PassedSteamroller
* PassedBinary Agents

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)
