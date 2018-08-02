---
layout: post
title: Day 7 of 100 Days Of Code
---
## Day 7: July 31, Tuesday

**Today 's Progress**: I continued the challanges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is a tough week I had another long day at work (counting the hellish commute) and was knee deep in DockerFiles CLI and RedHat's OpenShift. I feel like I could sleep for a whole day. Tomorrow it’s another long commute day. The Challenges seem hard, to me coming up with code from scratch is difficult it feels like a white board interview.

```javascript
//Find the Longest Word in a String
//Return the length of the longest word in the provided sentence.
function findLongestWordLength(str) {
    var obj = str.split(' ');// Split the words up
    var letterCount = 0; //variable for number of letters
    for (var i = 0; i < obj.length; i++) { //loop through the split string
        if (letterCount < obj[i].length) { // this looks ugly I'm sure there is a better way
            letterCount = obj[i].length;
        }
    }
    console.log(letterCount);
    return letterCount;    
} 
findLongestWordLength("The quick brown fox jumped over the lazy dog");
```

**Link(s) to work**
1.  Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

Introduction to Basic Algorithm Scripting

* PassedFind the Longest Word in a String
* PassedReturn Largest Numbers in Arrays

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)
