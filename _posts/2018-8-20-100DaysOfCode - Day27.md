---
layout: post
title: Day 27 of 100 Days Of Code
---

## Day 27: August 20, Monday

**Today 's Progress**: I continue work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on trying to define the challenge Caesar Cipher (or ROT13) and meet the requirements to pass This project. CaesarCipher.js is located here:[FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects).

After examining the requirements I made the following user story, As a user I want to: enter a ROT13 encoded string as input to a function which will returns a decoded plain text string. also:
* All letters will be uppercase.
* Do not transform any non-alphabetic character (i.e. spaces, punctuation), but be sure to pass them on in the result. I used the following:
* [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace),
* [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode),
* [ternary operator](https://www.w3schools.com/js/js_operators.asp)

```javascript
console.log("Caesars Cipher")
//Write a function which takes a ROT13 encoded string as input and returns a decoded string.
/***************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * CaesarsCipher, JJ 2018                                      *
 * https://repl.it/@JohnJohnson2/FCCProjectCaesarsCipher       *
 ***************************************************************/
//My solution
function rot13(str) { // LBH QVQ VG!
  let myStr = "";
  console.log(str + "");//Debugging str contents
  console.log((str + "").replace(/[A-Z]/gi, function (myStr) { return String.fromCharCode(myStr.charCodeAt(0) + (myStr.toLowerCase() < "n" ? 13 : -13));}));//Debugging conversion routine, should decode in ROT 13 or encode if plain text
  return (str + "").replace(/[A-Z]/gi, function (myStr) {
    return String.fromCharCode(myStr.charCodeAt(0) + (myStr.toLowerCase() < "n" ? 13 : -13));
  });
};
// Change the inputs below to test
rot13("SERR PBQR PNZC");
rot13("My Test");
```
This was not too hard but I did have some minor code problems that caused a couple refactoring of the code get the tests to pass. Then I wasn't happy and wanted to use ternary operator `?` and `.replace`.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedCaesars Cipher

All code is in GitHub and repl.it here: [repl.it FCCProjectCaesarsCipher](https://repl.it/@JohnJohnson2/FCCProjectCaesarsCipher) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)
