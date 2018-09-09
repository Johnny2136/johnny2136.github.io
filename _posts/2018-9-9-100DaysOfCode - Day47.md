---
layout: post
title: Day 47 of 100 Days Of Code
---

!["Done with REACT/Redux!"](https://derpicdn.net/img/view/2012/9/16/99468__safe_pinkie+pie_sweet+and+elite_animated_partillery_party+cannon.gif)

## Day 47: September 9, Sunday

**Today 's Progress**: Started working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Completed first project toward the Front End Certification at freecodecamp.

### Resources used:
  * [Example Quote generator](https://codepen.io/c-herr/pen/dNWjby),
  * [https://codepen.io/](https://codepen.io/)
  * [JSFiddle version](https://jsfiddle.net/johnny2136/oz4aqpyL/2/)

**Front End Libraries Projects - Build a Random Quote Machine**

  Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/qRZeGZ.

  Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.
  You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!
  - [x] User Story #1: I can see a wrapper element with a corresponding id="quote-box".
  - [x] User Story #2: Within #quote-box, I can see an element with a corresponding id="text".
  - [x] User Story #3: Within #quote-box, I can see an element with a corresponding id="author".
  - [x] User Story #4: Within #quote-box, I can see a clickable element with a corresponding id="new-quote".
  - [x] User Story #5: Within #quote-box, I can see a clickable element with a corresponding id="tweet-quote".
  - [x] User Story #6: On first load, my quote machine displays a random quote in the element with id="text".
  - [x] User Story #7: On first load, my quote machine displays the random quote's author in the element with id="author".
  - [x] User Story #8: When the #new-quote button is clicked, my quote machine should fetch a new quote and display it in the #text element.
  - [x] User Story #9: My quote machine should fetch the new quote's author when the #new-quote button is clicked and display it in the #author element.
  - [x] User Story #10: I can tweet the current quote by clicking on the #tweet-quote a element. This a element should include the "twitter.com/intent/tweet" path in it's href attribute to tweet the current quote.
  - [x] User Story #11: The #quote-box wrapper element should be horizontally centered. Please run tests with browser's zoom level at 100% and page maximized.

  You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
  Once you're done, submit the URL to your working project with all its tests passing.
  Remember to use the Read-Search-Ask method if you get stuck.

  Solution: https://codepen.io/johnny2136/pen/BOzEVz/

  * [JSFiddle version](https://jsfiddle.net/johnny2136/oz4aqpyL/2/)

  * [CodePen Example](https://codepen.io/johnny2136/pen/BOzEVz/)

```Javascript
const project_name = 'random-quote-machine';

const quotes = [{
  text: 'Well Bones, do the new medical facilities meet with your approval?',
  author: '-Kirk'
}, {
  text: 'Live long and prosper',
  author: '-Spock'
}, {
  text: 'Computers make excellent and efficient servants, but I have no wish to serve under them.',
  author: '-Spock'
}, {
  text: 'In critical moments, men sometimes see exactly what they wish to see.',
  author: '-Spock'
}, {
  text: 'When you eliminate the impossible, whatever remains, however improbable, must be the truth.',
  author: '-Spock'
}, {
text: 'The needs of the many outweigh the needs of the few.',
  author: '-Spock'
}, {
text: 'What am I, a doctor or a moon-shuttle conductor?',
  author: '-McCoy'
}, {
text: 'Resistance Is Futile',
  author: '-Borg '
}, {
text: 'In Space, all warriors are Cold Warriors.',
  author: '-Klingon Proverb'
}, {
  text: 'How we deal with death is at least as important as how we deal with life',
  author: '-Kirk'
}]

const textDiv = document.getElementById('text');
const authorDiv = document.getElementById('author');
const newQuoteBtn = document.getElementById('new-quote');
const tweetBtn = document.getElementById('tweet-quote');
let currentRnd = -1;

function fetchQuote() {
  let rnd;
  do {
    rnd = Math.floor(Math.random() * quotes.length)
  } while (currentRnd === rnd)

  currentRnd = rnd;

  textDiv.innerHTML = quotes[rnd].text;
  authorDiv.innerHTML = quotes[rnd].author;

  tweetBtn.setAttribute('href', `//twitter.com/intent/tweet?text=${textDiv.innerHTML}`)

}

(function() {
  fetchQuote();
})();

newQuoteBtn.addEventListener('click', () => {
  fetchQuote();
})
```
**Link(s) to work**

1. Started work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

* PassedBuild a Random Quote Machine

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).
