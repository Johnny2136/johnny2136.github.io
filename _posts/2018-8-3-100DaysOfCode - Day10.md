---
layout: post
title: Day 10 of 100 Days Of Code
---
## Day 10: August, Friday

**Today 's Progress**: I continued working the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is done this has been a trying week with very rough commutes today I left early and still had a 3 hour commute. We did more labs in OpenShift and probes in  CLI as well as configuring the GUI. The weekend is here and I plan on resting and knocking some FCC_Challenges out! Starting tonight. The Challenges, well I got stuck on the second one, and had to read more on `.filter` after that and some false starts I nailed it. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

```javascript
// Falsy Bouncer
//Remove all falsy values from an array.
//Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  return arr.filter(object => object);
  //or....
  //return arr.filter(Boolean);  
}
console.log(bouncer([7, "ate", "", false, 9]));
console.log(bouncer(["a", "b", "c"])); //should return ["a", "b", "c"].
console.log(bouncer([false, null, 0, NaN, undefined, ""])); //should return [].
console.log(bouncer([1, null, NaN, 2, undefined])); //should return [1, 2].
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedSlice and Splice
* PassedFalsy Bouncer
* PassedWhere do I Belong
* PassedMutations
All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)
