---
layout: post
title: Day 40 of 100 Days Of Code
---

![Image from XKCD](https://imgs.xkcd.com/comics/wisdom_of_the_ancients.png)

## Day 40: September, Sunday

**Today 's Progress**: I continued work on Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Redux and react are pretty crappy!

### Resources used:
  * [What listener() does in the Redux store?](https://stackoverflow.com/questions/36163442/what-listener-does-in-the-redux-store),
  * [Redux Dispatch With Event Listeners](https://learn.co/lessons/redux-dispatch-with-event-listeners)

```Redux
const ADD = 'ADD';
const reducer = (state = 0, action) => {
  switch(action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};
const store = Redux.createStore(reducer);
// global count variable:
let count = 0;
// change code below this line
const incrementCounter = () => count +=1
store.subscribe(incrementCounter);
// change code above this line
store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
```

This was a pretty hard challenge, instructions were not very clear at all and there were no examples.

**Link(s) to work**

1. Continued work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) (trying to) learn Redux.

**Introduction to the React Challenges**

* PassedDispatch an Action Event
* PassedHandle an Action in the Store
* PassedUse a Switch Statement to Handle Multiple Actions
* PassedUse const for Action Types

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).
