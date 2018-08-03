---
layout: post
title: Day 9 of 100 Days Of Code
---
## Day 9: August, Thursday

**Today 's Progress**: I continued working the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: Due to dentist appointment no commute today Yay!!!! :smile: I did my homework for the OpenShift class that I'm in this week and read over what they went over in class today. The Challenges continue to be difficult but I'm hanging in there with this 100-day coding challenge. JavaScript is a bit different from plain Java like the `findElement` of an array in Java it's `return Arrays.asList(arr).contains(targetValue);` and in Java script its `var found = array1.find(function(element)` Took me a while to get the one below.

```javascript
//Finders Keepers
//Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument). If no element passes the test, return undefined.
function findElement(arr, func) {
  var num;
  console.log(arr);// for Debugging
  //console.log(arr.find((num) => {return func(num)})); //for troubleshooting.
  return arr.find((num) => {return func(num)});
}
console.log(findElement([1, 2, 3, 4], num => num % 2 === 0));//should return 2.
console.log(findElement([1, 3, 5, 8, 9, 10], num => num % 2 === 0)); //should return 8.
console.log(findElement([1, 3, 5, 9], num => num % 2 === 0)); //should return undefined.
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedBooFinders Keepers
* PassedBoo who
* PassedTitle Case a Sentence

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)
