---
layout: post
title: Day 28 of 100 Days Of Code
---

## Day 28: August 21, Tuesday

**Today 's Progress**: I continue work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on the Telephone Number Validator challenge This is all about RegEx to pass This project. The telephoneNumberValidator.js is located here:[FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_JS_Projects/telephoneNumberValidator.js).

After examining the requirements I made the following user story, As a user I want to: pass a number to a function that returns true if the passed string looks like a valid US phone number.

For example: For this challenge you will be presented with a string such as 800-692-7753 or 8oo-six427676;laskdjf. Your job is to validate or reject the US phone number based on any combination of the formats provided above. The area code is required. If the country code is provided, you must confirm that the country code is 1. Return true if the string is a valid US phone number; otherwise return false.
* Sample validation data was provided.
* [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp),
* [regexpal.com](https://www.regexpal.com/index.php),
* [regex101.com](https://regex101.com/r/h2HCMZ/1/)

```javascript
/***********************************************************************
 * JavaScript Algorithms and Data Structures Projects:                 *
 * Telephone Number Validator, JJ 2018                                 *
 * https://repl.it/@JohnJohnson2/FCCProjectTelephoneNumberValidatorjs  *
 ***********************************************************************/
//My solution
function telephoneCheck(str) {
  // Good luck!
  //RegExp was validated here: https://regex101.com/r/h2HCMZ/1/
 var phoNum = /^(1\s?)?(\(\d{3}\)|\d{3})[\s\-]?\d{3}[\s\-]?\d{4}$/;
 console.log(phoNum.test(str));
 return phoNum.test(str);
};
//Tests Here:
telephoneCheck("555-555-5555");// should return a boolean.
telephoneCheck("1 555-555-5555");// should return true.
telephoneCheck("1 (555) 555-5555");// should return true.
telephoneCheck("5555555555");// should return true.
telephoneCheck("555-555-5555");// should return true.
telephoneCheck("(555)555-5555");// should return true.
telephoneCheck("1(555)555-5555");// should return true.
telephoneCheck("555-5555");// should return false.
telephoneCheck("5555555");// should return false.
telephoneCheck("1 555)555-5555");// should return false.
telephoneCheck("1 555 555 5555");// should return true.
telephoneCheck("1 456 789 4444");// should return true.
telephoneCheck("123**&!!asdf#");// should return false.
telephoneCheck("55555555");// should return false.
telephoneCheck("(6054756961)");// should return false
telephoneCheck("2 (757) 622-7382");// should return false.
telephoneCheck("0 (757) 622-7382");// should return false.
telephoneCheck("-1 (757) 622-7382");// should return false
telephoneCheck("2 757 622-7382");// should return false.
telephoneCheck("10 (757) 622-7382");// should return false.
telephoneCheck("27576227382");// should return false.
telephoneCheck("(275)76227382");// should return false.
telephoneCheck("2(757)6227382");// should return false.
telephoneCheck("2(757)622-7382");// should return false.
telephoneCheck("555)-555-5555");// should return false.
telephoneCheck("(555-555-5555");// should return false.
telephoneCheck("(555)5(55?)-5555");// should return false.
```
This also was not too hard but validating the regexp to get the tests to pass took a lot of time I actually started working on it yesterday.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedTelephone Number Validator

All code is in GitHub and repl.it here: [repl.it FCCProjectTelephoneNumberValidator.js](https://repl.it/@JohnJohnson2/FCCProjectTelephoneNumberValidatorjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)
