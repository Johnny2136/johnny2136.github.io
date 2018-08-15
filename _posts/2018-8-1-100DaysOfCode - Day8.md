---
layout: post
title: Day 8 of 100 Days Of Code
---
## Day 8: August 01, Wednesday

**Today 's Progress**: I continued working the challanges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is not getting any easier I had another long day at work (counting the hellish commute 2.5 hours to go 65 miles) we did more docker files in OpenShift and Dockerfiles CLI also RedHat's OpenShift GUI console. Tomorrow I have a dentist appointment and homework for the OpenShift class I'm in this week. The Challenges continue to be difficult but I'm hanging in there with this 100-day coding challenge.

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  var sln = target.length;
  console.log(sln);//Debugging statment
  if(str.substr(-sln) === target){
    console.log(str.substr(-sln) + " = " + target);//Debugging statment
    return true;
  } else {
    return false;
  }
}
confirmEnding("Bastian", "n");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedConfirm the Ending
* PassedRepeat a String Repeat a String
* PassedTruncate a String

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)
