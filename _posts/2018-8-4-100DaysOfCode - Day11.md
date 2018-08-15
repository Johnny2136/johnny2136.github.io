---
layout: post
title: Day 11 of 100 Days Of Code
---
## Day 11: August 04, Saturday

**Today 's Progress**: I finished the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) and started the [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: Felt good finishing some FCC_Challenges! The Challenges in the algorithm section were tough, there were no examples and vague instructions but I manages with the help of Stackoverflow to get them done OOP section seems easy Should get a lot done tomorrow. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) and [Stackoverflow](https://stackoverflow.com)

```javascript
//Chunky Monkey
//Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.
function chunkArrayInGroups(arr, size) {//My solution reusing slice and push
  var a = 0;      
  var result = [0];
  for(var i = 0; i < arr.length; i += size){
      console.log(a);//Debugging
      result.push(arr.slice(a, size +i));
      a += size;
  }
  console.log(result + " & " + arr); //Debugging
  return result;
}
console.log(chunkArrayInGroups(["a", "b", "c", "d","a", "b", "c", "d"], 2));
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Finished [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

   * PassedChunky Monkey

2. Started [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

   **Introduction to the Object Oriented Programming**

   * PassedCreate a Basic JavaScript Object

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)
