---
layout: post
title: Day 20 of 100 Days Of Code
---

## Day 20: August 13, Monday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: I need to find out why its so hard to do these Challenges, again today I spent hours trying to get something I thought should work to actually work. I used to think I was pretty good at coming up with logical algorithms for solving problems but I am really struggling nothing seems to work, maybe there are too many options `for` vice `map` and the concept of `callbacks` is hard for me to grasp, I will keep trying, maybe it will get easier with practice.

```javascript
console.log("Pig Latin");
//Translate the provided string to pig latin. Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay". If a word begins with a vowel you just add "way" to the end. Input strings are guaranteed to be English words in all lowercase.
function translatePigLatin(str) {
  var pigLatin = '';
  var RegExp = /[aeiou]/gi;
  if (str[0].match(RegExp)) {
    pigLatin = str + 'way';
    //console.log('Test 1st letter is a aeiou');
  } else if(str.match(RegExp) === null) {//added to get last test to pass.
    pigLatin = str + 'ay';
    //console.log('Test there are only consonants');
  } else {
    var vowelIndex = str.indexOf(str.match(RegExp)[0]);
    //console.log(vowelIndex = str.indexOf(str.match(RegExp)[0]));
    pigLatin = str.substr(vowelIndex) + str.substr(0, vowelIndex) + 'ay';
  }  
  console.log(pigLatin);
  return pigLatin;
}
translatePigLatin("consonant");// should return "onsonantcay
translatePigLatin("california");// should return "aliforniacay".
translatePigLatin("paragraphs");// should return "aragraphspay".
translatePigLatin("glove");// should return "oveglay".
translatePigLatin("algorithm");// should return "algorithmway".
translatePigLatin("eight");// should return "eightway".
translatePigLatin("myclm");// should return "eightway".
translatePigLatin("shmmnd");// should return "eightway".
console.log("<----------------------next exercise------------------------->");
```
This one seemed at first pretty straight forward but I couldn't get the last test to pass. I finally looked at the hints and saw I wasn't checking for consonants, I finally got it to work... [String.prototype.match()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match), [w3schools.com](https://www.w3schools.com/js/js_regexp.asp) and [Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedPig Latin
* PassedSearch and Replace
* PassedDNA Pairing
* PassedMissing letters

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)
