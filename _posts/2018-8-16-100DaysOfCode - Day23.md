---
layout: post
title: Day 23 of 100 Days Of Code
---

## Day 23: August 16, Wednesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Another long day and long commute, barely got through one challenge.

```javascript
console.log("Smallest Common Multiple");
//Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters. The range will be an array of two numbers that will not necessarily be in numerical order. For example, if given 1 and 3, find the smallest common multiple of both 1 and 3 that is also evenly divisible by all numbers between 1 and 3. The answer here would be 6.
function smallestCommons(arr) {
let max = Math.max(arr[0],arr[1]);
let min = Math.min(arr[0],arr[1]);
//console.log(max + " & " + min);//Debugging

  function smallComMulti(a, b){ //find smallest Common Multiple
    for(var i = 1; i <= b; i++){     
      if((i * a) % b === 0){
        //console.log(i * a);//Debugging
        return (i * a);
      }
    }   
  };    
  let myNum = smallComMulti(max, min);
  for(var ii = min + 1; ii < max; ii++) {    
    myNum = smallComMulti(myNum, ii);   
  }
  console.log(myNum);
  return myNum;
};
// test here
smallestCommons([1,5]);
console.log("<----------------------next exercise------------------------->");
```
I had to rely on the hints and [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference).

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSmallest Common Multiple

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)
