---
layout: post
title: Day 41 of 100 Days Of Code
---

![Image from React and Redux](http://onsen.io.s3-website-us-east-1.amazonaws.com/blog/content/images/2016/Jun/react_redux.png)

## Day 41: September 3, Monday

**Today 's Progress**: I continued work on Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Only two more Redux before I go on to React and Redux (I know lucky me) ambiguous instructions hardly no relevant examples I don't think these challenges are a good way to learn these two frameworks.

### Resources used:
  * [4 ways to dispatch actions with Redux](https://blog.bam.tech/developper-news/4-ways-to-dispatch-actions-with-redux),
  * [React Redux this.props.getClasses is not a function](https://stackoverflow.com/questions/50835770/react-redux-this-props-getclasses-is-not-a-function)

```Redux
const INCREMENT = 'INCREMENT'; // define a constant for increment action types
const DECREMENT = 'DECREMENT'; // define a constant for decrement action types
const counterReducer = (state = 0, action) => {
  switch(action.type){
  case INCREMENT:
    return state + 1;
    break;
  case DECREMENT :
    return state -1;
    break;
  default:
    return state;
  }  
}; // define the counter reducer which will increment or decrement the state based on the action it receives
const incAction = () => {
  return {
    type : INCREMENT
  }
}; // define an action creator for incrementing
const decAction = () => {  
  return {
    type: DECREMENT
  }  
}; // define an action creator for decrementing
const store = Redux.createStore(counterReducer); // define the Redux store here, passing in your reducers
```

Worst one yet!!! poor instructions and no clear examples expects you to look at past challenges..

**Link(s) to work**

1. Continued work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) (trying to) learn Redux.

**Introduction to the React Challenges**

* PassedRegister a Store Listener
* PassedCombine Multiple Reducers
* PassedSend Action Data to the Store
* PassedUse Middleware to Handle Asynchronous Actions
* PassedWrite a Counter with Redux
* PassedNever Mutate State
* PassedUse the Spread Operator on Arrays

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).
