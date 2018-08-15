---
layout: post
title: Day 21 of 100 Days Of Code
---

## Day 21: August 14, Tuesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Don't have much time tonight, only worked through two challenges. I started a third but didn't finish it.

```javascript
console.log("Convert HTML Entities");
//Convert the characters &, <, >, " (double quote), and ' (apostrophe), in a string to their corresponding HTML entities. (You got to be kidding me!!!)
 function convertHTML(str) {
      const htmlEnt={
        '&':'&amp;',
        '<':'&lt;',
        '>':'&gt;',
        '\"':'&quot;',
        '\'':"&apos;"
      };
  return str.split('').map(function(ojbect){//Use Split and map function to filter str.
        return htmlEnt[ojbect] || ojbect;
      }).join('');//Use .join prototype
  };  
//test here
console.log(convertHTML("Dolce & Gabbana")); //should return Dolce &​amp; Gabbana.
console.log(convertHTML("Hamburgers < Pizza < Tacos")); //should return Hamburgers &​lt; Pizza &​lt; Tacos.
console.log(convertHTML("Sixty > twelve")); //should return Sixty &​gt; twelve.
console.log(convertHTML('Stuff in "quotation marks"')); //should return Stuff in &​quot;quotation marks&​quot;.
console.log(convertHTML("Schindler's List")); //should return Schindler&​apos;s List.
console.log(convertHTML("<>")); //should return &​lt;&​gt;.
console.log(convertHTML("abc")); //should return abc.
console.log("<----------------------next exercise------------------------->");
```
This one used elements from previous Challenges.

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSorted Union
* PassedConvert HTML Entities
All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)
