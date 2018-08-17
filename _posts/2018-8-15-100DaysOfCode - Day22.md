---
layout: post
title: Day 22 of 100 Days Of Code
---

## Day 22: August 15, Wednesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Another long day and longer commute, barely got through two challenges.

```javascript
console.log("Sum All Primes");
//Sum all the prime numbers up to and including the provided number. A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two. The provided number may not be a prime.
function sumPrimes(num) {
  function myPrime(number){
      for (let i = 2; i <= number; i++){
          if(number % i === 0 && number!= i){
             return false;
          }
       }
    return true;
  };
  if (num === 1){
    return 0;
  };
  if(myPrime(num) === false){
    return sumPrimes(num - 1);
  };
  // Check if your number is prime
  if(myPrime(num) === true){
    return num + sumPrimes(num - 1);
  }
};
// test here
console.log(sumPrimes(10));
console.log("<----------------------next exercise------------------------->");
```
I had to rely on the hints to get this.

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSum All Odd Fibonacci Numbers
* PassedSum All Primes
All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)
