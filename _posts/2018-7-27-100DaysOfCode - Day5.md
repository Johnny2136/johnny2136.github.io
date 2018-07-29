-- -
layout: post
title: Day 4 of 100 Days Of Code
-- -
 ## Day 5: July 29, Sunday

 **Today 's Progress**: My goal today is to finnish the remaining challanges in [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures).

**Thoughts**: Remembered NO OVER THINKING!!! I have a bad habit of over complicating simple instructions, well it says do "a" I think well should i get to "a" via `ax^2+ab+c=0` :smile:

Today didn’t disappoint I forgot to capitalize the "O" in "Object" and spent almost an hour trying to figure why the unit tests weren’t passing ARGGGGG!!!

```javascript
//Generate an Array of All Object Keys with Object.keys()
//Finish writing the getArrayOfUsers function so that it returns an array containing all the properties in the object it receives as an argument.
let users2 = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};
function getArrayOfUsers(obj) {
  // change code below this line
  return Object.keys(obj);//OH GOD!!! an hour just because I forgot to capitalize O
  // change code above this line
}
console.log(getArrayOfUsers(users2));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedAdd Key-Value Pairs to JavaScript Objects
* PassedModify an Object Nested Within an Object
* PassedAccess Property Names with Bracket Notation
* PassedUse the delete Keyword to Remove Object Properties
* PassedCheck if an Object has a Property
* Passed Iterate Through the Keys of an Object with a for...in Statement
* PassedGenerate an Array of All Object Keys with Object.keys()
* PassedModify an Array Stored in an Object

All code is in GitHub and repl.it here: [Repl.it](https: //repl.it/@JohnJohnson2/FCCBasicDataStructurs2) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)
