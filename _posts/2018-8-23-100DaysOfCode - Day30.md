---
layout: post
title: Day 30 of 100 Days Of Code
---

![Image of buggy code](https://imgs.xkcd.com/comics/code_quality_3.png)

## Day 30: August 23, Thursday

**Today 's Progress**: I started work on [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass) I had completed a couple sections previously those were:
* [Introduction to the Bootstrap Challenges](https://learn.freecodecamp.org/front-end-libraries/bootstrap)
* [Introduction to jQuery](https://learn.freecodecamp.org/front-end-libraries/jquery)

**Thoughts**: The [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass) seem pretty buggy it makes a big difference to use Chrome. Firefox should work but in the last challenge I did I knew the code was correct based on [Sass Validator](https://www.sassmeister.com/) results, but the unit tests failed, so I tried the same code in chrome and it passed I'm not sure what the issue was.

### Resources used:
  * [Sass (Syntactically Awesome StyleSheets)](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)
  * [Sass Lang Guide](https://sass-lang.com/guide)
  * [Sass Validator](https://www.sassmeister.com/)

```html
#Use @for to Create a Sass Loop(Passes in Chrome)
<style type='text/sass'>
  @for $j from 1 to 6 {
    .text-#{$j} {font-size: 10px * $j; }
   }  
</style>

<p class="text-1">Hello</p>
<p class="text-2">Hello</p>
<p class="text-3">Hello</p>
<p class="text-4">Hello</p>
<p class="text-5">Hello</p>
```
To make it pass in Firefox... use:
```html
#Use @for to Create a Sass Loop(Passes in Firefox)
<style type='text/sass'>
  @for $j from 1 to 6 {
    .text-#{$j} {font-size: 10px * $j; }
   }  
</style>

<p class="text-1" style="font-size:10px;">Hello</p>
<p class="text-2" style="font-size:20px;">Hello</p>
<p class="text-3" style="font-size:30px;">Hello</p>
<p class="text-4" style="font-size:40px;">Hello</p>
<p class="text-5" style="font-size:50px;">Hello</p>
```
This also was a frustrating challenge I worked pretty hard getting the tests to pass. Took changing browsers (I did find a way to get the tests to pass in Firefox by adding style to P tags).

**Link(s) to work**

1. Started work on [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass).

**Introduction to the Sass Challenges**

* PassedStore Data with Sass Variables
* PassedNest CSS with Sass
* PassedCreate Reusable CSS with Mixins
* PassedUse `@if` and `@else` to Add Logic To Your Styles
* PassedUse `@for` to Create a Sass Loop

All code is in GitHub and repl.it here: [repl.it FCCProjectcashRegisterjs](https://repl.it/@JohnJohnson2/FCCProject-cashRegisterjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)
