---
layout: post
title: Day 26 of 100 Days Of Code
---

## Day 26: August 19, Sunday

**Today 's Progress**: I Started work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: I focused on trying to define the challenge and fully understand the requirements to pass these projects. This isn't like the other challenges as these are for the certification.  I made a place in the FCC-Projects repo on GitHub here in [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects) to store my projects. I had previously did the first project so moved on to the second today. my goal is to complete one a day but some may take longer.

After examining the requirements I made the following user story, As a user I want to: convert the given number into a roman numeral, and all roman numerals answers should be upper-case. I used the following:
* [Modulus (Division Remainder)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)
* [Array.lengthr](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length),
* [Assignment operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators)
* [Converting Decimal Number lying between 1 to 3999 to Roman Numerals](https://www.geeksforgeeks.org/converting-decimal-number-lying-between-1-to-3999-to-roman-numerals/),

```javascript
console.log("Roman Numeral Converter")
//Convert the given number into a roman numeral. All roman numerals answers should be provided in upper-case.
 /**************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * Roman Numeral Converter, JJ 2018                            *
 * https://jsfiddle.net/johnny2136/8m6937xd/20/                *
 ***************************************************************/
function convertToRoman(num) {
  //Make 2 arrays.
  const decArr = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];
  const romArr = ["M", "CM","D","CD","C", "XC", "L", "XL", "X","IX","V","IV","I"];
  //Variable for solution.
  let romNum = "";// Be carfull not to accidentally add whitespace
  //While loop inside a for to convert the Number to Roman number
  //console.log("Number: " + num);//Debugging
  for (let i = 0; i <= decArr.length; i++) {     
    while (num % decArr[i] < num) {
      //console.log(num);//Debugging
      romNum += romArr[i];       
      num -= decArr[i];
      //console.log(romNum);//Debugging
      //console.log(num);//Debugging
    };
  };
  console.log(romNum);
  return romNum;
};
//Unit tests:
convertToRoman(36);//should return "XXXVI"
convertToRoman(2); //should return "II".
convertToRoman(3); //should return "III".
convertToRoman(4); //should return "IV".
convertToRoman(5); //should return "V".
convertToRoman(9); //should return "IX".
convertToRoman(12); //should return "XII".
convertToRoman(16); //should return "XVI".
convertToRoman(29); //should return "XXIX".
convertToRoman(44); //should return "XLIV".
convertToRoman(45); //should return "XLV"
convertToRoman(68); //should return "LXVIII"
convertToRoman(83); //should return "LXXXIII"
convertToRoman(97); //should return "XCVII"
convertToRoman(99); //should return "XCIX"
convertToRoman(400); //should return "CD"
convertToRoman(500); //should return "D"
convertToRoman(501); //should return "DI"
convertToRoman(649); //should return "DCXLIX"
convertToRoman(798); //should return "DCCXCVIII"
convertToRoman(891); //should return "DCCCXCI"
convertToRoman(1000); //should return "M"
convertToRoman(1004); //should return "MIV"
convertToRoman(1006); //should return "MVI"
convertToRoman(1023); //should return "MXXIII"
convertToRoman(2014); //should return "MMXIV"
convertToRoman(3999); //should return "MMMCMXCIX"
```
This was pretty straight forward but I did have some minor code problems that caused hours of debugging to get the tests to pass.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedPalindrome Checker
* PassedRoman Numeral Converter

All code is in GitHub and repl.it here: [repl.it FCC_Projects_RomanNumeralConverter.js](https://repl.it/@JohnJohnson2/FCCProjects-RomanNumeralConverterjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)
