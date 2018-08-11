---
layout: post
title: Day 17 of 100 Days Of Code
---

## Day 17: August, Friday

**Today 's Progress**: I finished work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Some of these Challenges continue to be pretty hard while others very simple, I am dealing with the aggravating ones as well as the easy ones.

For example an easy one:
```javascript
//Introduction to Currying and Partial Application
//Fill in the body of the add function so it uses currying to add parameters x, y, and z.
function add(x) {
  // Add your code below this line
    return function(y) {
      return function(z) {
        return x + y + z;
      }
    }  
  // Add your code above this line
}
console.log(add(10)(20)(30));//should return 60.
console.log(add(1)(2)(3)); //should return 6.
console.log(add(11)(22)(33)); //should return 66.
//Your code should include a final statement that returns x + y + z.
console.log("-------------------Next------------------------");
```
And a Aggravating one:
```JavaScript
//Apply Functional Programming to Convert Strings to URL Slugs
//Fill in the urlSlug function so it converts a string title and returns the hyphenated version for the URL. You can use any of the methods covered in this section, and don't use replace. Here are the requirements:
//The input is a string with spaces and title-cased words
//The output is a string with the spaces between words replaced by a hyphen (-)
//The output should be all lower-cased letters
//The output should not have any spaces
// the global variable
var globalTitle = "Winter Is Coming";
// Add your code below this line
function urlSlug(title) {
console.log("First --> "+ title);//DEbugging
var myTitle = title.split(/\W+/); //from previous excersize
console.log("Second  --> "+ myTitle);//DEbugging
var filterTitle = myTitle.filter(function(obj){// my solution-Mozilla.org
return /\S/.test(obj);// Mozilla.org
});
console.log("Third  --> "+ filterTitle.join("-").toLowerCase());//DEbugging
console.log("Finally Global  --> "+ globalTitle);//DEbugging
return filterTitle.join("-").toLowerCase();// StackOverflow!!!
};// ARRRGGGGGHHH!!!!! This was hard!!!!!
// Add your code above this line
var winterComing = urlSlug(globalTitle); // Should be "winter-is-coming"
//Additional tests....
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");// should return "a-mind-needs-books-like-a-sword-needs-a-whetstone".
urlSlug("Hold The Door");// should return "hold-the-door".(https://stackoverflow.com/questions/6442327/using-split-join-to-replace-a-string-with-a-array)
//this challange sort of sucked!!! Took me a long time :(
//This helped https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test
//and this https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `split, filter, join` work togather... [StackOverflow.com]((https://stackoverflow.com/questions/6442327/using-split-join-to-replace-a-string-with-a-array))

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedReturn a Sorted Array Without Changing the Original Array
* PassedSplit a String into an Array Using the split Method
* PassedCombine an Array into a String Using the join Method
* PassedApply Functional Programming to Convert Strings to URL Slugs
* PassedUse the every Method to Check that Every Element in an Array Meets a Criteria
* PassedUse the some Method to Check that Any Elements in an Array Meet a Criteria
* PassedIntroduction to Currying and Partial Application

All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)
